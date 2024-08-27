# ui.Label Tutorial

## Introduction

The `ui.Label` is one of the simplest and most commonly used UI elements in `omni.ui`. It is used to display text within your UI. In this tutorial, we will learn how to create and customize labels.

## Prerequisites

- Basic understanding of Python.
- Nvidia Omniverse environment setup.

## Creating a Basic Label

To create a label, you use the `ui.Label` class. Below is an example of how to create a basic label in a window.

```python
import omni.ui as ui

# Create a window
window = ui.Window("Label Example", width=300, height=200)

# Create a label inside the window
with window.frame:
    ui.Label("Hello, Omniverse!")
```

## Change the text of a label

You can change the text of a label by using the `text` property.

```python
import omni.ui as ui

# Create a window
window = ui.Window("Label Example", width=300, height=200)

# Create a label inside the window
with window.frame:
    label = ui.Label("Hello, Omniverse!")
    label.text = "New Text"
```

## Customizing a Label

You can customize a label by setting various properties. For example, you can change the text color, font size, and alignment.

```python
import omni.ui as ui
from omni.ui import color as cl

# Create a window
window = ui.Window("Customized Label Example", width=300, height=200)

# Create a label inside the window
with window.frame:
    ui.Label("Customized Label", style={"font_size": 24, "color": cl("#097eff")})
```

## Summary

In this tutorial, we learned how to create and customize labels in `omni.ui`. We covered the basics of creating a label, changing its text, and customizing its appearance. Labels are essential for displaying text in your UI applications, and mastering them will help you create more sophisticated and informative user interfaces.