---
title: KeyFeature 1
menu_order: 1
---
<div class="tabs">
  <button class="tab-button" onclick="openTab(event, 'tab1')">Designer</button>
  <button class="tab-button" onclick="openTab(event, 'tab2')">Programmer</button>
</div>

<div id="tab1" class="tab-content">

<h2 id="development">Development</h2>
<h2 id="key-features">Key Features</h2>
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
