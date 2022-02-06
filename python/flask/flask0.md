# Notes from Corey's flask course 

We can put in `localhost:5000` instead of that `127.0.0.1:5000`
- In order not to close down the web server everytime we make changes, we can turn the `debug mode: ON` by saying:
```
set FLASK_DEBUG=1
```
then we dont have to `Ctrl+C` and rerun the server. Just `save`,`reload` and boom.

- to run this just with python without env variables

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def hello_world():
    return "<p>Hello, World!</p>"

if __name__=='__main__':
    app.run(debug=True)
```
and then just `python file_name.py`.

## Adding another route

Adding about page:
```python
@app.route("/about")
def about_greet():
    return "<h2>This is an about page.</h2>"
```

Adding multiple routes to same destination/page:
```python
@app.route("/")
@app.route("/home")
def home():
    return "<h2>This is a home page.</h2>"
```
Now, both `/` and `/home` will lead to the home page.

## Templates

- created the `templates` folder.
- created `about.html` and `home.html`
  
- added `render_template` to import statement and then change:
```python
def home():
    return "<p>Hello, World!</p>"
```
to:
```python
def home():
    return render_template('home.html')
```
Adding posts:(sample)
```python
posts= [
    {
        'author': 'Ken',
        'title': 'Blog Post 1',
        'content': 'First post content',
        'date_posted': 'April 30, 2021'
    }
]
```
and then add `posts(the var name)=posts` in render_template call line. And add `{% %}` into the html file and blah blah. 

Example template `code block`:
```html
{% for post in posts%} <!--'posts' is the second argument we have to put in the render template statement. (posts=posts)-->
        <h1>{{ post.title}}</h1>
        <p>By {{ post.author}} on {{ post.date_posted }}</p>
        <p>{{ post.content }}</p>
    {% endfor%}
```
If else statement:
```html
{% if title %}
        <title>Flask Blog - {{ title }}</title>
    {% else %}
        <title>Home page</title>
    {% endif %}
```
This statement means: if there is a title provided, use it as the title. Else, use the default title. *We can provide the title in the render_template statement.*
