# EasyButton
Buttons Component for Blazor

## What is EasyButton?

EasyButton contains button components for Blazor, which make it easier to use material design icons as button icons.

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

The design is not special, it looks like Bootstrap. But the IconButton makes it easier to use material design.
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

**Attributes for (standard) Button:**

| Attribute  | Description | Values |
| ------------- | ------------- |------------- |
| **Type**  | Translates to **type** attribute of an HTML button  |submit, reset, button. Default value is submit|
| **Color**  | Defines the color and style of the button. Currently available colors: blue, green, yellow, red. Each color has an outline version. |blue, blue-outline, green, green-outline, yellow, yellow-outline, red, red-outline.|
| **Corners** | Sets the corner type, default value is 4 px | noradius - for sharp corners; round - for round edges; leave out for default |
| **CssClass** | Translates to the HTML **class** attribute | |
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
