# Notes from FCC's tkinter course
Here we go.

>Code files in desktop/codefiles/tkinter

- hello.py

- Everything is a widget in tkinter
- Firstly, we need to create the basic frame widget window(main screen)
- First label and then put on screen.

Example(Hello World):
```python
from cgitb import text
from logging import root
from tkinter import *

# root window
root = Tk()

# creating a label widget
myLabel = Label(root, text="Goodbye World!")

# putting it onto the screen
myLabel.pack() 

#Then we need to put it into event loop(constant loop)
root.mainloop()

#When run it will show the text `Goodbye World`
```

09:35