# Working with Basic Input Fields in NVIDIA Omniverse

## Introduction

This tutorial covers three fundamental input fields in NVIDIA Omniverse: IntField, FloatField, and StringField. We'll explore how to create, use, and manipulate these fields using their models.

## Setup

First, import the necessary module:

```python
import omni.ui as ui
```

## 1. StringField

StringField is used for text input.

### Creating a StringField

```python
with ui.Window("String Input Example"):
    string_field = ui.StringField()
```

### Working with the StringField model

```python
# Set a value
string_field.model.set_value("Hello, Omniverse!")

# Get the current value
current_text = string_field.model.get_value_as_string()
print(f"Current text: {current_text}")

# Respond to changes
def on_string_changed(*args):
    value = string_field.model.get_value_as_string()
    print(f"Text changed to: {value}")

string_field.model.add_value_changed_fn(on_string_changed)
```

## 2. IntField

IntField is used for integer input.

### Creating an IntField

```python
with ui.Window("Integer Input Example"):
    int_field = ui.IntField()
```

### Working with the IntField model

```python
# Set a value
int_field.model.set_value(42)

# Get the current value
current_int = int_field.model.get_value_as_int()
print(f"Current integer: {current_int}")


# Respond to changes
def on_int_changed(*args):
    value = int_field.model.get_value_as_int()
    print(f"Integer changed to: {value}")

int_field.model.add_value_changed_fn(on_int_changed)
```

## 3. FloatField

FloatField is used for decimal number input.

### Creating a FloatField

```python
with ui.Window("Float Input Example"):
    float_field = ui.FloatField()
```

### Working with the FloatField model

```python
# Set a value
float_field.model.set_value(3.14)

# Get the current value
current_float = float_field.model.get_value_as_float()
print(f"Current float: {current_float}")

# Respond to changes
def on_float_changed(*args):
    value = float_field.model.get_value_as_float()
    print(f"Float changed to: {value:.2f}")

float_field.model.add_value_changed_fn(on_float_changed)
```

## Practical Tips

1. **Flexible Event Handlers**: Use `*args` in your value changed functions to make them more flexible and compatible with different callback signatures.

2. **Type Safety**: Always use the appropriate `get_value_as_*` method (e.g., `get_value_as_int()` for IntField) to ensure type safety.

3. **Change Tracking**: Use `add_value_changed_fn()` to respond to user input in real-time.

## Conclusion

These basic input fields - StringField, IntField, and FloatField - are fundamental building blocks for creating user interfaces in NVIDIA Omniverse. By understanding how to work with their models and how to set up flexible event handlers, you can create interactive and responsive UI elements in your Omniverse applications.