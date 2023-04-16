以下是一个使用 `@tailwindcss/utilities` 的示例代码，其中展示了其常用的 CSS 实用工具类及其能力：

```
html复制代码<!-- 响应式布局 -->
<div class="container mx-auto md:flex lg:flex-wrap">
  <div class="block bg-gray-200 p-4 md:w-1/2 lg:w-1/4">...</div>
  <div class="block bg-gray-200 p-4 md:w-1/2 lg:w-1/4">...</div>
  <div class="block bg-gray-200 p-4 md:w-1/2 lg:w-1/4">...</div>
  <div class="block bg-gray-200 p-4 md:w-1/2 lg:w-1/4">...</div>
</div>

<!-- 文本排版 -->
<p class="text-2xl font-bold text-center text-gray-700">Welcome to my website!</p>

<!-- 背景样式 -->
<div class="bg-gradient-to-br from-blue-500 to-indigo-500 h-64"></div>

<!-- Box Shadow -->
<div class="shadow-lg"></div>

<!-- 边框样式 -->
<div class="border border-gray-300 rounded-lg"></div>

<!-- 滚动条样式 -->
<div class="overflow-y-scroll scrollbar-thin scrollbar-thumb-gray-400"></div>

<!-- 表格样式 -->
<table class="w-full table-fixed">
  <thead>
    <tr>
      <th class="px-4 py-2 w-1/4">Name</th>
      <th class="px-4 py-2 w-1/4">Email</th>
      <th class="px-4 py-2 w-1/4">Age</th>
      <th class="px-4 py-2 w-1/4">City</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="border px-4 py-2">Alice</td>
      <td class="border px-4 py-2">alice@example.com</td>
      <td class="border px-4 py-2">25</td>
      <td class="border px-4 py-2">New York</td>
    </tr>
    <tr>
      <td class="border px-4 py-2">Bob</td>
      <td class="border px-4 py-2">bob@example.com</td>
      <td class="border px-4 py-2">30</td>
      <td class="border px-4 py-2">San Francisco</td>
    </tr>
  </tbody>
</table>

<!-- Flexbox -->
<div class="flex items-center justify-center space-x-4">
  <button class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded">Save</button>
  <button class="bg-gray-500 hover:bg-gray-600 text-white font-bold py-2 px-4 rounded">Cancel</button>
</div>

```

在这段代码中，我们使用了 `@tailwindcss/utilities` 提供的 CSS 实用工具类，实现了以下能力：

-   响应式布局：在 `container` 和 `flex` 相关的 CSS 实用类中，设置了不同屏幕宽度下的元素排列方式和间距。
-   文本排版：使用 `text-*` 系列的 CSS 实用类，设定了文字的大小、颜色等属性。
-   背景样式：使用 `bg-gradient-to-*` 系列的 CSS 实用类，设置了渐变背景色。
-   Box Shadow：使用 `shadow-*` 系列的 CSS 实用类，设定物品阴影的样式。
-   边框样式：使用 `border` 和 `rounded-*` 系列的 CSS 实用类，设定元素的边框样式和圆角。
-   滚动条样式：使用 `scrollbar-*` 系列的 CSS 实用类，设定列表或容器内部滚动条的样式。
-   表格样式：使用 `table` 和 `border` 系列的 CSS 实用类，设定表格的边框和单元格样式。
-   Flexbox：使用 `flex` 和 `space-x-*` 系列的 CSS 实用类，支持 Flexbox 布局。

以上是 `@tailwindcss/utilities` 提供的一些能力的示例代码，其余的实用工具类也可以在官方文档中找到。