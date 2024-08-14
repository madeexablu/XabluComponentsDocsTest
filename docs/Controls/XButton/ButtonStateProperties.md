---
title: StateProperties
menu_order: 4
taxonomy:
    doc_category: documentation
---

# StateProperties

The StateProperties are the intended way to alter the visuals of any component. It is assumed that you have read the [general page](/documentation/state-properties.md) with information about the workings of the StateProperties.

## ButtonStateProperties

The key for the ButtonStateProperties is defined as follows:
| Key         | Type               | Options                                                           |
| ----------- | ------------------ | ----------------------------------------------------------------- |
| ButtonType  | ButtonTypes        | `Primary`<br>`SecondaryFilled`<br>`SecondaryOutlined`<br>`Action` |
| VisualState | ButtonVisualStates | `Normal`<br>`Pressed`<br>`Disabled`                               |

For any combination of ButtonType and VisualState the following properties can be set to change the visuals of the Button.

| Property         | Type   | Description                                                                     |
| ---------------- | ------ | ------------------------------------------------------------------------------- |
| BackgroundColor  | Color  | BackgroundColor of the Button.                                                  |
| TextColor        | Color  | Color of the Text of the Button.                                                |
| BorderColor      | Color  | Color of the outer border.                                                      |
| InnerBorderColor | Color  | Color of the inner border.                                                      |
| BorderWidth      | double | Width of the border of the outer border of the Button.                          |
| LeftIconTint     | Color  | Color of the left icon of the Button. If not set, the TextColor will be taken.  |
| RightIconTint    | Color  | Color of the right icon of the Button. If not set, the TextColor will be taken. |

## Example

### Xaml

```xml
<xablu:XButton  ButtonType="SecondaryFilled"
                LeftIconSource="icon_check_circle.png"
                RightIconSource="icon_chevron_down.png"
                Text="Button">
    <xablu:XButton.StateProperties>
        <xablu:ButtonStateProperties
            ButtonType="SecondaryFilled"
            VisualState="Normal"
            BackgroundColor="Black"
            LeftIconTint="Red"
            TextColor="Green"
            RightIconTint="Blue"
            BorderWidth="5" />
    </xablu:XButton.StateProperties>
</xablu:XButton>
```
