# ui.Button Tutorial

## Introduction

The `ui.Button` is used to create interactive buttons in `omni.ui`. This tutorial will show you how to create buttons and handle button click events.

## Prerequisites

- Basic understanding of Python.
- Nvidia Omniverse environment setup.

## Creating a Basic Button

To create a button, you use the `ui.Button` class. Below is an example of how to create a basic button and handle a click event.

```python
import omni.ui as ui

# Create a window
window = ui.Window("Button Example", width=300, height=200)

# Create a button inside the window
with window.frame:
    def on_button_click():
        print("Button clicked!")
    
    ui.Button("Click Me", clicked_fn=on_button_click)
```

## Customizing a Button

You can customize a button by setting its text, icon, and other properties. Below is an example of how to create a button with a custom icon and text.

```python
import omni.ui as ui
from omni.ui import color as cl

window = ui.Window("Customized Button", width=300, height=200)
with window.frame:
    def on_button_click():
        print("Styled button clicked!")
    
    ui.Button(
        "Styled Button",
        clicked_fn=on_button_click,
        style={"background_color": cl.('#097eff')}
    )
```


## Summary

In this tutorial, we learned how to create and handle button click events in `omni.ui`. We covered the basics of creating a button and handling click events. Buttons are essential for creating interactive UI applications in Nvidia Omniverse, and mastering them will help you create more sophisticated and user-friendly interfaces.