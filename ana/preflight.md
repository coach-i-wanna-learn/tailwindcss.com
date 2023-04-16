https://github.com/tailwindlabs/tailwindcss/blob/master/src/css/preflight.css

`Preflight` 是 Tailwind 的一个插件，提供了一套基础样式规则，用于解决浏览器间的一些不兼容性问题，并为开发者提供了更好的可定制性。

具体来说，`Preflight` 在 `@tailwind base` 中被注入，它包含了一组固定的 CSS 样式规则，能够帮助开发者在不同浏览器之间实现一致的默认样式。这些规则在整个 Tailwind 项目中都会被自动注入，以确保你的项目在不同浏览器中能够呈现出一致的表现效果。

与 `@tailwind components` 和 `@tailwind utilities` 不同的是，`Preflight` 中的样式规则通常是不太会被注意到的。但是这些规则是很有必要的，因为它们可以消除浏览器之间的不一致性，让你的项目更加稳定可靠。

参考来源：

-   \[[1](https://tailwindcss.com/docs/preflight)\]
-   \[[2](https://www.tailwindcss.cn/docs/preflight)\]


`@tailwind base` 包含了一组基础样式规则，这些规则涵盖了 HTML 元素的默认样式、CSS 属性的默认值等。具体而言，包含以下样式：

-   `box-sizing` 属性的值被修改为 `border-box`。
-   `margin` 和 `padding` 属性的默认值被设置为 `0`。
-   `list-style` 属性的默认样式被设置为 `none`。
-   `font-family` 属性的默认字体列表被设置为系统字体列表和默认字体。
-   `font-size` 属性的默认值被设置为 `16px`。
-   `line-height` 属性被设置为相对于父元素的百分比。
-   `text-align` 属性被设置为 `left`。
-   `break-word` 属性被启用，使长单词和 URL 可以换行。

除了这些样式之外，`@tailwind base` 还包括一些修改通用 HTML 元素的样式规则，例如标题（`h1`\-`h6`）、段落（`p`）以及列表（`ul` 和 `ol`）等。

需要注意的是，`@tailwind base` 会重置一些默认样式，因此在项目中可以自定义样式以覆盖这些默认样式。