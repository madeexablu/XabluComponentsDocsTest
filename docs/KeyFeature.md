---
title: KeyFeature 2
menu_order: 1
---
<div class="tabs">
  <button class="tab-button" onclick="openTab(event, 'tab1')">Programmer</button>
  <button class="tab-button" onclick="openTab(event, 'tab2')">Designer</button>
</div>

<div id="tab1" class="tab-content">

<h1 id="key-features">Key Features</h2>
<table>
<thead>
<tr>
<th>Property Name</th>
<th>Type</th>
<th>Default</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>AvatarType</td>
<td>AvatarTypes<br><br>Enum Values:<br><code>Text</code><br><code>ImageFit</code><br><code>ImageFill</code></td>
<td>Text</td>
<td>Sets the type of the Avatar.</td>
</tr>
<tr>
<td>SizeType</td>
<td>AvatarSize<br><br>Enum Values:<br><code>XXXS</code><br><code>XXS</code><br><code>XS</code><br><code>S</code><br><code>M</code><br><code>L</code><br><code>XL</code><br><code>XXL</code><br><code>XXXL</code><br><code>XXXXL</code></td>
<td>M</td>
<td>Sets the size of the Avatar.<br> Note: SizeType <code>XXXS</code> is not supported in combination with AvatarType <code>ImageFit</code></td>
</tr>
<tr>
<td>Text</td>
<td>string</td>
<td>default(string)</td>
<td>Sets the text of the avatar component when the AvatarType is <code>Text</code></td>
</tr>
<tr>
<td>IconSource</td>
<td>ImageSource</td>
<td>null</td>
<td>The source for the image that is displayed when AvatarType is <code>ImageFit</code> or <code>ImageFill</code></td>
</tr>
</tbody>
</table>
<h2 id="using-the-avatar">Using the Avatar</h2>
<p>The following sample shows the steps to consume and use the Avatar component.</p>
<p>1. Add the Xablu namespace in XAML:</p>
<pre><code class="lang-xml"><span class="hljs-symbol">xmlns:</span>xablu=<span class="hljs-string">"https://schemas.xablu.com/2023/components"</span>
</code></pre>
<p>2. Define the XAvatar in XAML:</p>
<pre><code class="lang-xml"><span class="hljs-tag">&lt;<span class="hljs-name">VerticalStackLayout</span>&gt;</span>
    <span class="hljs-tag">&lt;<span class="hljs-name">xablu:XAvatar</span>  <span class="hljs-attr">AvatarType</span>=<span class="hljs-string">"ImageFill"</span>
                    <span class="hljs-attr">SizeType</span>=<span class="hljs-string">"XL"</span>
                    <span class="hljs-attr">IconSource</span>=<span class="hljs-string">"profile_image.png"</span> /&gt;</span>
<span class="hljs-tag">&lt;/<span class="hljs-name">VerticalStackLayout</span>&gt;</span>
</code></pre>

</div>

<div id="tab2" class="tab-content">
<h1 id="key-features">Key Features</h1>
<p>There are two properties defined in Figma in the Avatar component:</p>
<ul>
<li>SizeType</li>
<li>AvatarType</li>
</ul>
<h2 id="sizetype">SizeType</h2>
<p>10 different SizeTypes are predefined. Ranging from 3xs to 4xl. These can be used in different scenarios. <br> A smaller size is advised in a navigation bar, but on a profile page a larger size can be displayed for example. </br></p>
<h2 id="avatartype">AvatarType</h2>
<p>There are three types initials, imageFit, or ImageFill. Which to use depends on the scenario</p>
<ul>
<li><strong>ImageFit</strong> indicates that the total image fits within the whole circle. This value is advised to be used for icons. </li>
<li><strong>ImageFill</strong> indicates that the image is cropped to be a circle. This type is advised to be used for pictures. </li>
<li><strong>Initials</strong> can be used in scenarios where e.g. an image is lacking. </li>
</ul>
<p>See the overview page for a visual illustration of the difference betweeen ImageFill and ImageFit.</p>
<h2 id="avatar-content">Avatar Content</h2>
<p>Depending on the chosen type, the content should be set as follows</p>
<table>
<thead>
<tr>
<th>AvatarType</th>
<th>How to set content</th>
</tr>
</thead>
<tbody>
<tr>
<td>ImageFit</td>
<td>The icon can be set at the nested component <strong>AvatarXDS</strong> with the property IconSource</td>
</tr>
<tr>
<td>ImageFill</td>
<td>The image can be changed by setting another image as backgroundcolor to the avatar</td>
</tr>
<tr>
<td>Initials</td>
<td>The initials can be set at the nested component <strong>Avatar XDS</strong> with the property Text</td>
</tr>
</tbody>
</table>
<h2 id="other-customization">Other customization</h2>
<p>Besides the predefined properties within Figma, there are a few other things that can be customised. </p>
<h3 id="color-changes">Color changes</h3>
<ul>
<li>BackgroundColor</li>
<li>BorderColor</li>
<li>TextColor (For AvatarType Initials)</li>
</ul>
<p>Sizes and forms cannot be adjusted at the moment for avatars. </p>

</div>
