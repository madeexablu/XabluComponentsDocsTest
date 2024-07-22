---
title: KeyFeature 3
menu_order: 1
---

<div class="tabs">
  <button class="tab-button" onclick="openTab(event, 'tab1')">Designer</button>
  <button class="tab-button" onclick="openTab(event, 'tab2')">Programmer</button>
</div>

<div id="tab1" class="tab-content">
  <!-- Placeholder for tab1 content -->
  {{% tab1-content %}}
</div>

<div id="tab2" class="tab-content">
  <!-- Placeholder for tab2 content -->
  {{% tab2-content %}}
</div>

<script>
function openTab(evt, tabName) {
  var i, tabcontent, tabbuttons;
  tabcontent = document.getElementsByClassName("tab-content");
  for (i = 0; i < tabcontent.length; i++) {
    tabcontent[i].style.display = "none";
  }
  tabbuttons = document.getElementsByClassName("tab-button");
  for (i = 0; i < tabbuttons.length; i++) {
    tabbuttons[i].className = tabbuttons[i].className.replace(" active", "");
  }
  document.getElementById(tabName).style.display = "block";
  evt.currentTarget.className += " active";
}
</script>

<!-- Content for tab1 -->
{{% tab1-content %}}
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

1. Add the Xablu namespace in XAML:

```xml
xmlns:xablu="https://schemas.xablu.com/2023/components"
```

2. Define the XAvatar in XAML:

```xml
<VerticalStackLayout>
    <xablu:XAvatar  AvatarType="ImageFill"
                    SizeType="XL"
                    IconSource="profile_image.png" />
</VerticalStackLayout>
```

<!-- Content for tab2 -->
{{% tab2-content %}}
## Programmer Section

Content for the Programmer tab goes here.
```

### Explanation:

1. **HTML Structure for Tabs**: The HTML structure and JavaScript function for switching tabs are defined as before.
2. **Content Placeholders**: Use placeholders (e.g., `{{% tab1-content %}}` and `{{% tab2-content %}}`) to denote where the Markdown content for each tab should go.
3. **Markdown Content**: Define the actual Markdown content for each tab outside the HTML divs, using the same placeholders to ensure the content is properly rendered.

### Note:
The placeholders (`{{% tab1-content %}}` and `{{% tab2-content %}}`) are used to logically separate content. You need to replace these placeholders with a method your Markdown processor or template engine supports to include content. If you're using a specific Markdown processor that supports partials or includes, you should use the appropriate syntax.

If your Markdown processor does not support this kind of placeholder syntax directly, you may need to manually split the file into multiple sections and ensure they are correctly rendered in the final output. The key is to avoid wrapping the Markdown content directly inside the HTML divs.
