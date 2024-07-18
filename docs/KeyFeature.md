---
title: KeyFeature 1
menu_order: 1
---
<div class="tabs">
  <button class="tab-button" onclick="openTab(event, 'tab1')">Designer</button>
  <button class="tab-button" onclick="openTab(event, 'tab2')">Programmer</button>
</div>

<div id="tab1" class="tab-content">

## Development

## Key Features

| Property Name | Type                                                                                                                 | Default         | Description                                                                                                       |
| ------------- | -------------------------------------------------------------------------------------------------------------------- | --------------- | ----------------------------------------------------------------------------------------------------------------- |
| AvatarType    | AvatarTypes<br><br>Enum Values:<br>`Text`<br>`ImageFit`<br>`ImageFill`                                               | Text            | Sets the type of the Avatar.                                                                                      |
| SizeType      | AvatarSize<br><br>Enum Values:<br>`XXXS`<br>`XXS`<br>`XS`<br>`S`<br>`M`<br>`L`<br>`XL`<br>`XXL`<br>`XXXL`<br>`XXXXL` | M               | Sets the size of the Avatar.<br> Note: SizeType `XXXS` is not supported in combination with AvatarType `ImageFit` |
| Text          | string                                                                                                               | default(string) | Sets the text of the avatar component when the AvatarType is `Text`                                               |
| IconSource    | ImageSource                                                                                                          | null            | The source for the image that is displayed when AvatarType is `ImageFit` or `ImageFill`                           |

## Using the Avatar

The following sample shows the steps to consume and use the Avatar component.

1\. Add the Xablu namespace in XAML:

```xml
xmlns:xablu="https://schemas.xablu.com/2023/components"
```

2\. Define the XAvatar in XAML:

```xml
<VerticalStackLayout>
    <xablu:XAvatar  AvatarType="ImageFill"
                    SizeType="XL"
                    IconSource="profile_image.png" />
</VerticalStackLayout>
```

</div>
