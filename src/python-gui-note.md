# Python with Kivy in GUI Development

Kivy is a free and open source Python framework for GUI development.

- **Installment**

```command
# install Kivy framework
pip install kivy
```

- **Hello World Demo**

```python
from kivy.app import App
from kivy.uix.button import Button

class TestApp(App):
  def build(self):
    return Button(text = "Hello World")

TestApp().run()
```

Execute the Program:

```command
python demo.py
```

![image](https://user-images.githubusercontent.com/15795237/159803147-5232cc3e-1b46-4de9-be7d-f91ebaec3e25.png)
