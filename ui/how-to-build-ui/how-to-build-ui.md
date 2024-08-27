# Create a User Interface in Nvidia Omniverse

Nvidia Omniverse is a powerful platform that enables creators, developers, and engineers to build real-time simulations, collaborate on 3D design, and much more. One of the key components of creating interactive applications within Omniverse is building a user interface (UI). This tutorial will guide you through the steps to build a basic UI using the omni.ui framework.

## What is omni.ui?

omni.ui is a flexible and powerful framework in Omniverse for building user interfaces. It provides a wide range of widgets, layout management, and customization options, allowing you to create sophisticated and interactive UIs tailored to your application's needs.

## Step 1: Setting Up Your Development Environment

Before diving into UI creation, ensure that your Omniverse development environment is set up. You can follow the guideline here: https://github.com/NVIDIA-Omniverse/kit-app-template. But I am also going to create a Tutorial on how to setup your own application. Make sure to create an extension and open it in your IDE of choice so you can follow along.


## Step 2: Creating a New UI Window

Start by creating a new window that will house your UI elements. This is done by instantiating a Window object in your extension's Python script.

```python
import omni.ui as ui
import omni.ext

class MyExtension(omni.ext.IExt):
    def on_startup(self, ext_id):
        self._window = ui.Window("My Window", width=400, height=300)
        with self._window.frame:
            self._build_ui()
```
This code snippet creates a window titled "My Window" with a specified width and height. The - with self._window.frame: - block is where you'll build the actual UI.

## Step 3: Building the UI Layout

Next, define the layout for your UI components. Omniverse offers various layout containers such as VStack (Vertical Stack), HStack (Horizontal Stack), and Grid. These help organize your UI elements effectively.

```python
def _build_ui(self):
    with ui.VStack():
        ui.Label("Welcome to Omniverse!")
        ui.Button("Click Me", clicked_fn=self._on_button_click)
```
In this example, a vertical stack is used to align a label and a button. The clicked_fn parameter links the button to a callback function that handles the click event.

## Step 4: Adding Interactivity with Widgets

Omniverse's omni.ui provides a wide range of widgets that you can add to your UI, such as sliders, checkboxes, text fields, and more.

```python
def _on_button_click(self):
    print("Button clicked!")
```

Here we have the callback function for our ui.Button.

## Step 5: Advanced Layouts and Widgets

For more complex UIs, you can use advanced widgets and layouts. For example, CollapsableFrame allows sections of your UI to be collapsed or expanded, which is useful for organizing large UIs. Or ScrollingFrame to make your UI scrollable

```python	
with ui.ScrollingFrame():
    with ui.VStack():
        with ui.CollapsableFrame("Advanced Settings"):
            ui.Label("Adjust the parameters below:")
            ui.Button("Push the button")
```

## Step 6: Testing and Debugging

Omniverse supports hot-reloading, which means you can test your UI in real-time as you develop it. This is invaluable for iterating on your design quickly. Make sure to test your UI thoroughly to ensure it behaves as expected.

## Step 7: Add content to your created extension

If you like you can create an extension like we did in [Creating First Extension](../basics/creating-first-extension/creating-first-extension.md) and add your UI to it.

## Conclusion

Creating a user interface in Omniverse using omni.ui is a straightforward process thanks to the framework's powerful features and flexibility. I have to admit that some advanced features are not intuitive but when you get the hang on it you can craft nice UI pretty fast.