**Since Bootstrap released their own set of icons and Bootstrap 5, their buttons work very well with icons now. Thus, this component is not longer required or maintained.**

# EasyButton v.1.0.1
Buttons Component for Blazor

## What is EasyButton?

EasyButton contains button components for Blazor, which make it easier to use material design icons as button icons. It uses (requires) Bootstrap for the design.


## How can it be used?

You can download it as a NuGet package and reference it in your Blazor project.
https://www.nuget.org/packages/EasyButton/

Then you simply use it like other components.

    <EasyButton.IconButton Type="submit" Text="Save">
        <span class="material-icons-outlined">
            done
        </span>
    </EasyButton.IconButton>

## Why use it?

The design is not special (uses Bootstrap). But the IconButton makes it easier to use material design icons.
You simply copy and paste the icon span between the button tags.

## Layout examples:

![image](https://user-images.githubusercontent.com/70850868/128259811-13cab841-2f11-42cd-84bd-0a6ed171bd17.png)

## Documentation

**Using the components**

To use the buttons in your pages you have two possibilities

1. The plain button: Use like standard button with the button text between the tags.
```
<EasyButton.Button>Submit</EasyButton.Button>
```

2. The IconButton: Place the icon span between the tags and pass the button text through the **Text** attribute.
```
<EasyButton.IconButton Text="Submit">
        <span class="material-icons">done</span>
<EasyButton.IconButton>
```

For both types there is a number of attributes that can be used to change the button's appearance.
Use Bootstrap btn- classes to change the colors. The button already contains the "btn" class. It only requires the btn- +color class.

**Attributes for (standard) Button:**

| Attribute  | Description | Values |
| ------------- | ------------- |------------- |
| **Type**  | Translates to **type** attribute of an HTML button  |submit, reset, button. Default value is submit|
| **Corners** | Sets the corner type, default value is 4 px | noradius - for sharp corners; round - for round edges; leave out for default |
| **CssClass** | Translates to the HTML **class** attribute. Use Bootstrap classes here | e.g. "btn-outline-danger" |
| **Style** | Translates to the HTML **style** attribute | |
| **OnClick** | Replaces the @onclick="" attribute, but is used the same way: OnClick="EventHandlerMethod" | Name of the event handler method |

**Attributes for IconButton:**

**In addition to the above mentioned attributes*

| Attribute  | Description | Values |
| ------------- | ------------- |------------- |
| **Text**  | Sets the buttons text, since the space between the tags is reserved for the icon span | |

**Using icons**:

To use material icons follow the Developer guide: https://developers.google.com/fonts/docs/material_icons

**Event handling**:

The button is compatible with the click event. It can be invoked using **OnClick** attribute.

**Version notes**
v.1.0.1 - 08.08.2021
Removed css classes: 
    - button, all color classes
Functions changed:
    - Color attribute removed
    - instead implemented usage of Bootstrap button btn- classes
