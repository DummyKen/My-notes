# Notes from Jim Shaped Coding's Flask Course
- made a folder 'FlaskMarket'
- `pip install flask`
- Minimal Application:
```python
from flask import Flask

app = Flask(__name__)

@app.route("/") #decorator
def hello_world():
    return "<p>Hello, World!</p>"
```
- setting up environment variables:
```
set FLASK_APP=market.py
$env:FLASK_APP = "market.py"
```
and then hit
```
python -m flask run
```
and it will start running. *And I have to make a new folder as this folder is fucked up now:

Modify the html inside the python file:
```python
return """<h1>Heyyyylolo</h1>
<h2>Yooo</h2>
<hr>"""
```
- `Debug mode` should be on :
```
set FLASK_DEBUG=1
$env:FLASK_DEBUG = 1

```
I think it would be like `live server`. Yeah. 

**Everytime I set up an environment variable here in VSCode's terminal, I have to type in powershell command: `$env:....` to actually make it work dont know why.**