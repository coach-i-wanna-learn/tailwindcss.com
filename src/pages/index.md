## 设置 meta
```html
<Head>
  <meta
    key="twitter:title"
    name="twitter:title"
    content="Tailwind CSS - Rapidly build modern websites without ever leaving your HTML."
  />
  <meta
    key="og:title"
    property="og:title"
    content="Tailwind CSS - Rapidly build modern websites without ever leaving your HTML."
  />
  <title>Tailwind CSS - Rapidly build modern websites without ever leaving your HTML.</title>
</Head>
```


## 移动优先

```html
  <div className="mb-20 overflow-hidden sm:mb-32 md:mb-40">
```

优先设置移动端的样式，然后使用响应式类设置其他屏幕尺寸的样式

比如

```html
class="hidden md:flex items-center"
```

这个表示在移动端的尺寸下，隐藏，大屏展示

## rem

在前端开发中，rem（即 root em）是一种基于 HTML 根元素的相对长度单位。它的大小随设置在 `html` 标签上的字体大小而变化，被广泛用于响应式设计等场景。

使用 rem 单位可以方便地实现对不同屏幕尺寸的适配，也可以减少对具体像素的依赖，提高页面的可维护性。下面是如何使用 rem 的步骤：

1.  在 HTML 的头部添加 `<meta name="viewport" content="width=device-width,initial-scale=1">`，这个标签的作用是让页面根据设备的真实宽度进行缩放，保证在不同屏幕上都能正常显示。
2.  在 CSS 中使用 `rem` 单位，例如：`font-size: 1.4rem;`，这里的 `1rem` 等于根元素的字体大小。我们可以在根元素上设置一个字体大小，例如：`html {font-size: 16px;}`。
3.  当页面需要适配不同的屏幕尺寸时，可以通过 media query 或 JavaScript 来动态改变根元素的字体大小。

需要注意的是，在使用 rem 时，尽量不要使用绝对定位、固定宽度和高度等会受到具体屏幕尺寸影响的样式，避免出现布局错乱的情况。

参考来源：

-   \[[1](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Building_blocks/Values_and_units)\]
-   \[[2](https://www.w3cplus.com/css/define-font-size-with-css-root.html)\]


HTML 默认的 `font-size` 是 16px。这是因为在浏览器中，如果没有设置根元素（即 `html` 标签）的 `font-size`，默认情况下会使用浏览器的默认值，通常是16px。

在实际开发中，我们可以通过在 CSS 中设置根元素的 `font-size`，然后使用相对单位（如 `rem`、`em` 等）来进行页面布局和样式设置。这样，根据根元素设置的不同字体大小，相对单位的数值也会自动适应缩放，实现页面的响应式布局。

参考来源：

-   \[[2](https://developer.mozilla.org/en-US/docs/Web/HTML)\]
-   \[[4](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size)\]


## inset

`inset` CSS 属性的作用是设置元素相对于其包含块（即父级元素或容器）的位置。该属性可以同时设置元素的上、右、下、左四个方向的位置，也可以只设置任意一个或几个方向的位置。

具体来说，`inset` 属性可以实现以下效果：

1.  设置元素与其包含块的间距：可以通过调整 `inset` 属性的值，使元素与其包含块之间产生一定的间距效果。
    
2.  实现绝对定位：通过设置元素的定位方式（如 `position: absolute;`），再通过 `inset` 属性设置元素在包含块中的精确位置，可以实现绝对定位效果。
    

需要注意的是，与其他类似作用的属性（如 `margin` 和 `padding` 等）不同，`inset` 属性对于文本流和元素的盒模型并没有影响，因此该属性不会导致任何布局上的变化。

参考来源：

-   \[[1](https://developer.mozilla.org/en-US/docs/Web/CSS/Inset)\]
-   \[[2](https://www.w3schools.com/cssref/css_pr_inset.asp)\]


`inset` CSS 属性是一个缩写属性，用于设置元素相对于其包含块的位置。该属性可以设置元素的上、右、下、左四个方向的位置。

使用 `inset` 属性时，可以同时设置四个方向的值，也可以只设置两个或一个方向的值。若不设置某一方向的值，它会被设置为 auto。

以下是 `inset` 属性的几种使用方式：

1.  设置所有四个方向的值为相同的固定像素值
    
    ```
    css复制代码.box {
      inset: 10px; /* 上下左右均设置为 10px */
    }
    
    ```
    
2.  通过指定顺序分别设置顶部、右侧、底部、左侧的位置值
    
    ```
    css复制代码.box {
      inset: 20px 30px 40px 50px; /* 分别设置上、右、下、左的位置值 */
    }
    
    ```
    
3.  只设置某些方向的位置值
    
    ```
    css复制代码.box {
      inset: 20px auto 40px auto; /* 只设置上下方向的位置值 */
    }
    
    ```
    

需要注意的是，与其他具有方向性的属性（如 `margin-top` 和 `margin-bottom` 等）不同，`inset` 属性对于文本流和元素的盒模型并没有影响，因此该属性不会导致任何布局上的变化。

参考来源：

-   \[[1](https://developer.mozilla.org/en-US/docs/Web/CSS/Inset)\]
-   \[[2](https://www.w3schools.com/cssref/css_pr_inset.asp)\]


## 'clsx' 的作用，使用方式



根据来源 [2](https://www.npmjs.com/package/clsx)，可以得知，`clsx` 是一款 JavaScript 的工具库，它提供了一种方便的方式来生成不同的 CSS 类名字符串。

通常，前端开发者会在组件中使用 `clsx` 函数来根据不同的组件状态（比如交互状态、选中状态、禁用状态等）来生成具有不同 CSS 类名的 class 字符串。这些 class 字符串将被用于样式定义，从而实现样式的变化效果。

`clsx` 的使用方式是：在项目中安装 clsx 模块，然后在代码中引入和使用 clsx 函数。clsx 函数会多次调用，并将其返回值作为 class 字符串的一部分合并在一起。

下面是一个使用 clsx 实现动态生成 CSS 类名的例子：

```
javascript复制代码import clsx from 'clsx';
import React from 'react';

function Button(props) {
  const { className, variant, disabled, onClick } = props;

  // 注意：此处的 classnames 可以使用模板字符串或对象的方式进行构建，具体详见文档。
  const classnames = clsx(className, {
    'btn': true,
    'btn-disabled': disabled,
    'btn-primary': variant === 'primary',
    'btn-secondary': variant === 'secondary'
  });

  return (
    <button className={classnames} onClick={onClick}>
      {props.children}
    </button>
  );
}

export default Button;

```

在这个例子中，`clsx` 函数被用来将多个 class 字符串合并在一起。传入的第一个参数 `className` 为组件上已有的 class 名称，第二个参数则是根据组件状态（variant、disabled 等）动态生成的类名。最终合并后的 class 名称将会被应用到组件上，从而达到样式变化的效果。

需要注意的是，`clsx` 并不仅仅只能在 React 中使用，它可以应用于任何 JavaScript 项目中。

## styles.beams

这里直接使用 . 获取 css 文件中的 beams 样式

效果为

```css
.index_beams__yWcJT {
    background-image: url(/_next/static/media/hero@75.b2469a49.jpg);
    background-size: 150rem;
}
```

## bg-grid-slate-900/[0.04]
tailwindcss.com/tailwind.config.js 定义的特定格式解析成的特殊格式，-slate-900/[0.04] 是传入的参数

```
{
  'bg-grid': (value) => ({
    backgroundImage: `url("${svgToDataUri(
      `<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32" width="32" height="32" fill="none" stroke="${value}"><path d="M0 .5H31.5V32"/></svg>`
    )}")`,
  }),
},
```

```
url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32' width='32' height='32' fill='none' stroke='rgb(15 23 42 / 0.04)'%3e%3cpath d='M0 .5H31.5V32'/%3e%3c/svg%3e")'%3e%3cpath d='M0 .5H31.5V32'/%3e%3c/svg%3e)
```

## linear-gradient

`linear-gradient()` 是一个 CSS 函数，用于创建线性渐变背景。它的语法如下：

```
复制代码background: linear-gradient([<angle>|to <side-or-corner>],
  <color-stop1> [<color-stop-position1>],
  [<color-stop2> <color-stop-position2>],
  ..., 
  [<color-stopN> <color-stop-positionN>]);

```

其中，`<angle>` 或 `to <side-or-corner>` 用于定义渐变的方向。如果使用 `<angle>`，可以指定一个角度值（如 `45deg`），表示从该角度开始进行渐变；如果使用 `to <side-or-corner>`，可以使用关键字（如 `top`、`right bottom` 等），表示从一个方向开始进行渐变。

`<color-stop>` 可以指定渐变中的位置和颜色值。`<color-stop-position>` 指定了该颜色在渐变中的位置，可以为百分比或长度值。如果未指定该位置，则渐变将平均分配整个渐变范围。如果省略最后一个位置，则将其视为 `100%`。

以下是一些示例：

```
复制代码/* 从左到右的蓝色到红色渐变 */
background: linear-gradient(to right, blue, red);

/* 从上到下的绿、黄、红颜色渐变 */
background: linear-gradient(green, yellow, red);

/* 从左上到右下的渐变，同时指定每个颜色的位置 */
background: linear-gradient(to bottom right, 
  blue 0%, green 30%, yellow 70%, red 100%);

/* 使用角度指定渐变方向，从左下到右上的渐变 */
background: linear-gradient(45deg, blue, red);

```

当用angle参数来指定渐变方向时，正数值表示按顺时针方向的偏移角度，而负数值是按逆时针方向的偏移角度值。45度是时针指向1:30时的方向，90度是时针指向3:00时的方向，315度是时针指向10:30时的方向，0度/360度是时针指向12:00时的方向。因此，angle值为-45度和315度时所表示的激变方向指向是相同的。

参考资料：

-   \[[1](https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/linear-gradient)\]
-   \[[2](https://www.w3schools.com/css/css3_gradients_linear.asp)\]


## text-slate-700

查看 tailwind 颜色预设： https://tailwindcss.com/docs/customizing-colors

`text-slate-700` 是 Tailwind CSS 提供的文本颜色类，它表示文本颜色为深灰色。这是 Tailwind CSS 预定义的一组颜色之一，其命名规则是由颜色名称（如 `slate`）和颜色深度值（如 `700`）组成的。

具体来说，`text-slate-700` 这个 class 可以在 HTML 元素上应用，如下：

```
html复制代码<p class="text-slate-700">这是一段深灰色的文本。</p>

```

这将把该段落的文本颜色设置为深灰色。

参考资料：

-   \[[2](https://tailwindcss.com/docs/text-color)\]

## flex 默认主轴方向

Selected Text
Entire Document
Include front/back template
仅用于开发学习交流
Flex 的默认主轴方向是从左到右的，即 `flex-direction` 属性的默认值为 `row`，其中 `row` 表示主轴方向是水平方向，起点在左侧，终点在右侧。这个信息来源于 MDN \[[3](https://developer.mozilla.org/zh-CN/docs/Web/CSS/flex-direction)\]。


## slate 石板色的，深蓝灰色的

## font-

https://tailwindcss.com/docs/font-weight

| Class | Properties |
| --- | --- |
| font-thin | font-weight: 100; |
| font-extralight | font-weight: 200; |
| font-light | font-weight: 300; |
| font-normal | font-weight: 400; |
| font-medium | font-weight: 500; |
| font-semibold | font-weight: 600; |
| font-bold | font-weight: 700; |
| font-extrabold | font-weight: 800; |
| font-black | font-weight: 900; |


## text-sm（font-size）
https://tailwindcss.com/docs/font-size

| Class | Properties |
| --- | --- |
| text-xs | font-size: 0.75rem; /\* 12px \*/ line-height: 1rem; /\* 16px \*/ |
| text-sm | font-size: 0.875rem; /\* 14px \*/ line-height: 1.25rem; /\* 20px \*/ |
| text-base | font-size: 1rem; /\* 16px \*/ line-height: 1.5rem; /\* 24px \*/ |
| text-lg | font-size: 1.125rem; /\* 18px \*/ line-height: 1.75rem; /\* 28px \*/ |
| text-xl | font-size: 1.25rem; /\* 20px \*/ line-height: 1.75rem; /\* 28px \*/ |
| text-2xl | font-size: 1.5rem; /\* 24px \*/ line-height: 2rem; /\* 32px \*/ |


## leading
```css
.leading-6 {
    line-height: 1.5rem;
}
```

## 无障碍 sr-only

`sr-only` 是 Tailwind 中的一个类名，它用于屏幕阅读器用户。这个类名的作用是让屏幕阅读器将被标记的元素读出来，但在视觉上不会显示出来，从而使页面更加无障碍。如果你需要同时让元素在获得焦点时显示出来，可以结合使用 `sr-only` 和 `focus: sr-only` 类名。

`sr-only` 类名不仅存在于 Tailwind 中，也存在于 Bootstrap\[[3](https://getbootstrap.com/docs/4.0/utilities/screenreaders/)\]\[[4](https://getbootstrap.com/docs/5.0/getting-started/accessibility/)\]中。不过需要注意的是，在 Tailwind 和 Bootstrap 的版本中， `sr-only` 类名的具体实现可能会有所不同。

参考资料：

-   \[[1](https://tailwindcss.com/)\]
-   \[[3](https://getbootstrap.com/docs/4.0/utilities/screenreaders/)\]
-   \[[4](https://getbootstrap.com/docs/5.0/getting-started/accessibility/)\]


## 手写 svg

```html
<path d="m19 19-3.5-3.5" />
<circle cx="11" cy="11" r="6" />
```

这段 SVG 代码表示一个包含圆形和路径两个元素的图形。具体来说：

-   `<circle cx="11" cy="11" r="6" />` 表示一个圆形元素，其中 `cx` 和 `cy` 属性用于指定圆心的 x 和 y 坐标， `r` 属性用于设置圆的半径，这里圆心坐标为 (11, 11)，半径为 6。
-   `<path d="m19 19-3.5-3.5" />` 表示一个路径元素，其中 `d` 属性用于定义路径数据。这里的路径数据是 `m19 19-3.5-3.5`，其中 `m` 表示将画笔移动到指定位置，并从该位置开始绘制路径，后面的数字则分别表示 x 和 y 坐标的值。因此，这里的路径表示将画笔移动到坐标 (19, 19)，然后向左上方移动 3.5 个单位。

注意，虽然这两个元素在代码中是并列出现的，但它们实际上是分别独立的图形，它们之间没有任何关联或重叠。如果想要让它们组成一个整体，需要使用一些其他的 SVG 元素及其属性进行组合和布局。

### svg 包含的元素

下面是所有 SVG 图形元素的代码示例：

1.  `<rect>` 元素，用于绘制矩形：

```html
<svg>
  <rect x="10" y="10" width="100" height="50" />
</svg>

```

2.  `<circle>` 元素，用于绘制圆形：

```html
<svg>
  <circle cx="50" cy="50" r="40" />
</svg>

```

3.  `<ellipse>` 元素，用于绘制椭圆：

```html
<svg>
  <ellipse cx="50" cy="50" rx="40" ry="20" />
</svg>

```

4.  `<line>` 元素，用于绘制直线段：

```html
<svg>
  <line x1="10" y1="10" x2="100" y2="50" />
</svg>

```

5.  `<polyline>` 元素，用于绘制折线：

```html
<svg>
  <polyline points="10,10 50,50 90,10" fill="none" stroke="black" />
</svg>

```

6.  `<polygon>` 元素，用于绘制多边形：

```html
<svg>
  <polygon points="50,10 10,50 50,90 90,50" fill="none" stroke="black" />
</svg>

```

7.  `<path>` 元素，用于绘制任意路径：

```html
<svg>
  <path d="M10 10 L50 50 L90 10" fill="none" stroke="black" />
</svg>

```

8.  `<text>` 元素，用于在 SVG 中添加文字：

```html
<svg>
  <text x="50" y="50" font-size="20">Hello World!</text>
</svg>

```

除此之外，还有其他一些元素，如 `<image>` 用于添加图片、`<use>` 用于重复使用已有的图形元素等，可以根据具体需要进行选择和使用。

## search button 组件设计思路

动静分离，SearchButton 只有 button 元素 + 搜索逻辑，svg 是从外部传入的，扩展性更好

## -mr-1 负数的 margin-right

## gap-x-8

```css
.gap-x-8 {
    column-gap: 2rem;
}
```

在 CSS 中，`column-gap` 属性用于设置元素列之间的间距（即 gutter）。它是多列布局中的一部分，可以通过它来设置列之间的间距大小。根据 Box Alignment 规范，它也可以用于多列、弹性盒子（flexbox）和网格布局（grid layouts）等多种布局方式中。\[[2](https://developer.mozilla.org/en-US/docs/Web/CSS/column-gap)\]




## mx-auto 实现居中

`margin: auto` 属性可以用于实现元素在水平方向上的居中。它的原理是利用了自动外边距（auto margins）的特性，通过设置左右外边距为 `auto`，使得浏览器将左右外边距平均分配，从而实现水平居中的效果。

同时，如果要实现一个元素在垂直方向上的居中，还需要另外处理。具体方法有多种，常见的有使用绝对定位，或者使用 flexbox 等 CSS 技术。

关于使用绝对定位实现垂直居中的原理，可以参考互联网知识来源链接 \[1\] 中提到的内容。

而使用 flexbox 实现垂直和水平居中则更加简单，只需要设置父元素为 `display: flex; justify-content: center; align-items: center;` 即可。

\[[1](https://blog.csdn.net/ws9029/article/details/113851118)\]

## letter-spacing 
https://tailwindcss.com/docs/letter-spacing#customizing-your-theme

Letter Spacing

## ring

https://tailwindcss.com/docs/ring-width

box-shadow