# note-css-order
> CSS 伪类、伪元素、规则、以及属性的速查列表，根据 [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS) 归纳整理。  

* [Pseudo-classes 伪类](#pseudo-classes-伪类)
* [Pseudo-elements 伪元素](#pseudo-elements-伪元素)
* [At-rule 规则](#at-rule-规则)
* Properties 属性  
    * [summary 概要列表](#summary-list)  
    * [detail  详细列表](#detail-list)

###  Pseudo-classes 伪类   
[↑ top](#note-css-order)
>需要查询完整的规范内容？[Selectors Level 4](https://drafts.csswg.org/selectors-4/)  

``` css

    /* Logical Combinations */
    :matches() /*:any()*/   /* 匹配 集合内指定 的元素 */
    :not()                  /* 排除 满足指定关系 的元素 */
    :has()                  /* 匹配 满足指定关系 的元素*/


    /* Linguistic Pseudo-classes */
    :dir()                  /* 匹配 设置dir(文字书写方向)属性 的元素 */
    :lang()                 /* 匹配 设置lang(定义元素语言)属性 的元素 */


    /* Location Pseudo-classes */
    :any-link               /* 匹配 任意有链接锚点 的元素*/
    :link                   /* 匹配 未处于访问记录中 的链接 */
    :visited                /* 匹配 处于访问记录中 的链接 */
    :target                 /* 匹配 URL指向的锚点 的元素 */
    :scope                  /* 匹配 设置scoped属性的style标签 的作用域 */


    /* User Action Pseudo-classes */
    :hover                  /* 匹配 处于鼠标悬停状态 的元素 */
    :active                 /* 匹配 处于激活状态 的元素 */
    :focus                  /* 匹配 处于聚焦状态 的元素 */
    :focus-ring             /* 匹配 处于聚焦状态元素 的UA样式(聚焦轮廓) */
    :focus-within           /* 匹配 子节点处于聚焦状态 的元素 */
    :drop                   /* 匹配 处于拖拽状态 的元素 */
    :drop()                 /* 匹配 处于指定拖拽状态 的元素 */


    /* Time-dimensional Pseudo-classes */
    :current                /* 匹配 处于当前状态 的定义了timeline属性的元素 */
    :past                   /* 匹配 处于过去状态 的定义了timeline属性的元素 */
    :future                 /* 匹配 处于将来状态 的定义了timeline属性的元素 */


    /* Resource State Pseudos */
    :playing                /* 匹配 处于播放状态 的元素 */
    :paused                 /* 匹配 处于暂停状态 的元素 */


    /* The Input Pseudo-classes */
    :enabled                /* 匹配 可以编辑 的元素 */
    :disabled               /* 匹配 禁止编辑 的元素 */
    :read-only              /* 匹配 内容只读 的元素 */
    :read-write             /* 匹配 内容可编辑 的元素 */
    :placeholder-shown      /* 匹配 显示字段占位符文本 的元素 */
    :default                /* 匹配 页面载入默认选中 的元素 */

    :checked                /* 匹配 选中状态 的元素 */
    :indeterminate          /* 匹配 模糊状态 的元素 */

    :valid                  /* 匹配 输入内容通过类型验证 的元素 */
    :invalid                /* 匹配 输入内容无法通过类型验证 的元素 */
    :in-range               /* 匹配 输入数值符合范围 的元素 */
    :out-of-range           /* 匹配 输入数值溢出范围 的元素 */
    :required               /* 匹配 设置必填属性 的元素 */
    :optional               /* 匹配 可选字段 的元素 */
    :user-invalid           /* 匹配 用户输入内容未通过验证 的元素 */

    /* Tree-Structural pseudo-classes */
    :root                   /* 匹配 文档树 的根元素*/
    :empty                  /* 匹配 无子节点 的元素 */
    :blank                  /* 匹配 仅包含空格或者换行符 的元素 */

    :nth-child(n)           /* 匹配 符合元素集合中指定位置 的元素 */
    :nth-last-child(n)      /* 反序匹配 符合元素集合内指定位置 的元素 */
    :first-child            /* 匹配 符合元素集合内首个 的元素 */
    :last-child             /* 匹配 符合元素集合内末尾 的元素 */
    :only-child             /* 匹配 无兄弟节点 的元素 */

    :nth-of-type(n)         /* 匹配 符合元素集合中同类型指定位置 的元素 */
    :nth-last-of-type(n)    /* 反序匹配 符合元素集合中同类型指定位置 的元素 */
    :first-of-type          /* 匹配 每个在元素集合中初次出现 的元素 */
    :last-of-type           /* 匹配 每个在元素集合中末次出现 的元素 */
    :only-of-type           /* 匹配 无同类兄弟节点 的元素*/


    /* Fullscreen API */
    :fullscreen             /* 匹配 全屏显示模式中 的元素 */


    /* Page Selectors */
    :first                  /* 打印文档时首页的样式 */
    :left                   /* 打印文档时左侧的样式 */
    :right                  /* 打印文档时右侧的样式 */

```  

### Pseudo-elements 伪元素   
[↑ top](#note-css-order)
>需要查询完整的规范内容？[CSS Pseudo-Elements Module Level 4](https://www.w3.org/TR/css-pseudo-4/)   

``` css

    /* Typographic Pseudo-elements */
    ::first-line            /* 选取文字块首行字符 */
    ::first-letter          /* 选取文字块首行首个字符 */

    /* Highlight Pseudo-elements */
    ::selection             /* 选取文档中高亮(反白)的部分*/
    ::inactive-selection    /* 选取非活动状态时文档中高亮(反白)的部分*/
    ::spelling-error        /* 选取被 UA 标记为拼写错误的文本 */
    ::grammar-error         /* 选取被 UA 标记为语法错误的文本 */

    /* Tree-Abiding Pseudo-elements */
    ::before                /* 在选中元素中创建一个前置的子节点 */
    ::after                 /* 在选中元素中创建一个后置的子节点 */
    ::marker                /* 选取列表自动生成的项目标记符号 */
    ::placeholder           /* 选取字段的占位符文本(提示信息) */
    
    /* WebVTT Format */
    ::cue                   /* 匹配所选元素中 WebVTT 提示 */

    /* Fullscreen API */
    ::backdrop              /* 匹配全屏模式下的背景 */

```   

###  At-rule 规则   
[↑ top](#note-css-order)
>需要查询完整的内容？[MDN-CSS At-rule](https://developer.mozilla.org/en-US/docs/Web/CSS/At-rule)   

``` css

    @charset ;                              /* 声明样式表的字符集 */
    @import ;                               /* 引入一个外部样式表 */
    @namespace ;                            /* 使用 XML 命名空间 */

    @media () {/*...*/};                    /* 符合媒体查询后块内的样式生效 */
    @supports() {/*...*/};                  /* 检查到CSS属性可用后块内样式生效 */
    @document() {/*...*/};                  /* 符合文档条件后块内样式生效*/
    @page {/*...*/};                        /* 文档进行打印时的样式变化 */
    @font-face {/* ... */};                 /* 声明字体属性集 */
    @keyframes {/*...*/};                   /* 描述 CSS 动画的变化过程 */
    @viewport {/*...*/};                    /* 控制移动设备的视窗尺寸 */
    @counter-style {/*...*/};               /* 声明计数器(counter)样式 */
    @font-feature-values {/*...*/};         /* 定义字体特定的替换和花饰 */
    
```   

### Properties 属性   
>需要查询完整的内容？[MDN-CSS reference](https://developer.mozilla.org/zh-CN/docs/Web/CSS/Reference) 
#### summary list   
[↑ top](#note-css-order)
``` css
    ┌── 布局定位
    |   ├── 元素定位
    |   |   └── position...
    |   └── 元素浮动
    |       └── float...
    |—— 盒子模型
    |   ├── 盒子类型
    |   |   ├── display
    |   |   ├── 弹性盒子
    |   |   |   └── flex...
    |   |   ├── 网格系统
    |   |   |   └── grid...
    |   |   ├── 表格模型
    |   |   |   └── table-layout...
    |   |   ├── 列表盒子
    |   |   |   └── list-style...
    |   |   └── 标注模型
    |   |       └── ruby-align...
    |   ├── 盒子属性
    |   |   ├── box-sizing
    |   |   ├── 盒子尺寸
    |   |   |   ├── width...
    |   |   |   ├── height...
    |   |   |   ├── padding...
    |   |   |   ├── border...
    |   |   |   ├── outline...
    |   |   |   └── margin...
    |   |   └── 盒子样式
    |   |       ├── color
    |   |       ├── background...
    |   |       ├── background-blend-mode...
    |   |       ├── clip-path
    |   |       ├── mask...
    |   |       ├── filter
    |   |       ├── box-shadow
    |   |       ├── opacity
    |   |       └── visibility
    |   └── 盒子内容
    |       ├── 溢出处理
    |       |   └── overflow...
    |       ├── 垂直对齐
    |       |   └── vertical-align
    |       ├── 内容分列
    |       |   └── columns...
    |       ├── 文本渲染
    |       |   ├── 排版模式
    |       |   |   └── writing-mode...
    |       |   ├── 文本样式
    |       |   |   ├── text-rendering
    |       |   |   ├── font-feature-settings...
    |       |   |   └── font...
    |       |   ├── 文本控制
    |       |   |   ├── text-overflow
    |       |   |   ├── white-space
    |       |   |   ├── overflow-wrap...
    |       |   |   ├── word-break...
    |       |   |   ├── text-align...
    |       |   |   ├── font-synthesis
    |       |   |   ├── font-size-adjust
    |       |   |   ├── letter-spacing...
    |       |   |   └── text-transform...
    |       |   └── 文本装饰
    |       |       ├── quotes
    |       |       ├── tab-size
    |       |       ├── text-indent
    |       |       ├── text-emphasis...
    |       |       ├── text-decoration...
    |       |       └── text-shadow
    |       └── 图片元素
    |           ├── image-rendering...
    |           └── shape-image-threshold...
    |—— 盒子变形
    |   ├── transform-style...
    |   ├── perspective...
    |   └── backface-visibility
    |—— 动态效果
    |   ├── 过渡动画
    |   |   ├── transition...
    |   |   └── animation...
    |   └── 滚动效果
    |       └── scroll-behavior...
    └── 其他属性
        ├── 用户行为
        |   ├── resize
        |   ├── cursorresize...
        |   ├── touch-action
        |   ├── caret-color
        |   └── ime-mode
        ├── 元素属性
        |   └── object-fit
        |   ├── object-position
        |   ├── content
        |   ├── counter-reset...
        |   ├── will-change
        |   ├── pointer-events
        |   ├── z-index
        |   └── all
        ├── 定义变量
        |   └── --*
        └── 页面打印
            ├── page-break-before...
            └── widows

```  
#### detail list   
[↑ top](#note-css-order)

``` css

<length>:      .em | .ex | .ch | .rem | .lh | .rlh | .vh | .vw | .vi | .vb | .wmin | .vmax | .px | .mm | .cm | .in | .pt | .pc | .mozmm;
<percentages>: .%;
<url>:         url();
<number>:      1 | 1.1 | -1 | +1;
<integer>:     1 | -1 | +1;
<color>:       <hex-color> | <named-color> | transparent | currentcolor | rgb() | hsl() | rgba() | hsla() | <deprecated-system-color>;
<time>:        .ms | .s;


div {

    /* ------------------------------------------------ */
    /* -------------------- 布局定位 ------------------- */
    /* ------------------------------------------------ */

    /* ---------------------------- */
    /* ---------- 元素定位 --------- */
    /* ---------------------------- */

    /* 元素的定位方式 */
    position: static | relative | absolute | fixed | sticky;
        /* 使定位后的元素产生位置偏移 */
        top:    <length> | <percentages> | auto;
        right:  <length> | <percentages> | auto;
        bottom: <length> | <percentages> | auto;
        left:   <length> | <percentages> | auto;

    /* ---------------------------- */
    /* ---------- 元素浮动 --------- */
    /* ---------------------------- */

    /* 元素浮动 */
    float: left | right | none | inline-start | inline-end;
    /* 是否清除浮动 */
    clear: none | left | right | both | inline-start | inline-end;

    /* ------------------------------------------------ */
    /* -------------------- 盒子模型 ------------------- */
    /* ------------------------------------------------ */

    /* ---------------------------- */
    /* ---------- 盒子类型 --------- */
    /* ---------------------------- */

    /* 定义元素的盒子类型 */
    display: none | inline | block | list-item | inline-list-item | inline-block | inline-table | table | table-cell | table-column | table-column-group | table-footer-group | table-header-group | table-row | table-row-group | flex | inline-flex | grid | inline-grid | run-in | ruby | ruby-base | ruby-text | ruby-base-container | ruby-text-container | contents;

    /* ------------------- */
    /* ----- 弹性盒子 ----- */
    /* ------------------- */

    /* 项目的空间分配 */
    [-] flex: auto | initial | none | ...;
        /* 定义项目的拉伸因子 */
        flex-grow:   <number>;
        /* 定义项目的收缩规则 */
        flex-shrink: <number>;
        /* 指定项目在主轴方向的初始大小 */
        flex-basis:  <length> | <percentages> | content;
    /* 容器的主轴方向和换行规则 */
    [-] flex-flow: ...;
        /* 定义主轴的方向 */
        flex-direction: row | row-reverse | column | column-reverse;
        /* 声明是否允许换行 */
        flex-wrap:      nowrap | wrap | wrap-reverse;
    /* 项目在主轴上的空间分配 */
    justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
    /* 如何分配侧轴的空间位置 */
    align-content:   flex-start | flex-end | center | space-between | space-around | stretch;
    /* 项目在侧轴上的空间分配 */
    align-items:     flex-start | flex-end | center | baseline | stretch;
    /* 独立声明项目在侧轴上的空间分配 */
    align-self:      auto | flex-start | flex-end | center | baseline | stretch;
    /* 项目的排序权重 */
    order:           <integer>;

    /* ------------------- */
    /* ----- 网格系统 ----- */
    /* ------------------- */

    /* 网格容器属性 */
    [-] grid: ...;
        /* 横向网格线名称和网格高度 */
        grid-template-rows:    none | auto | [linename] | <length> |  <percentage> | <flex> | max-content | min-content | minmax() |   fit-content() | repeat();
        /* 纵向网格线名称和网格宽度 */
        grid-template-columns: none | auto | [linename] | <length> |  <percentage> | <flex> | max-content | min-content | minmax() |   fit-content() | repeat();
        /* 设置网格区域名称 */
        grid-template-areas:   none | <string> | .;
        /* 声明隐式网格行*/
        grid-auto-rows:        auto | <length> | <percentage> | <flex> |  max-content | min-content | minmax();
        /* 声明隐式网格列*/
        grid-auto-columns:     auto | <length> | <percentage> | <flex> |  max-content | min-content | minmax() | fit-content();
        /* 网格流的方向 */
        grid-auto-flow:        row | column | dense;
        /* 网格列的间距 */
        grid-column-gap:       <length> | <percentage>;
        /* 网格行的间距 */
        grid-row-gap:          <length> | <percentage>;
    /* 网格容器行列属性 */
    [-] grid-template: ...;
        grid-template-rows: ;
        grid-template-columns: ;
        grid-template-areas: ;
    /* 网格行列间距 */
    [-] grid-gap: ...;
        grid-row-gap: ;
        grid-column-gap: ;
    /* 项目空间位置 */
    [-] grid-area: <custom-ident> | ...;
        /* 项目行的初始位置 */
        grid-row-start:    auto | span | <integer> | <custom-ident>;
        /* 项目行的结束位置 */
        grid-row-end:      auto | span | <integer> | <custom-ident>;
        /* 项目列的初始位置 */
        grid-column-start: auto | span | <integer> | <custom-ident>;
        /* 项目列的结束位置 */
        grid-column-end:   auto | span | <integer> | <custom-ident>;
    /* 项目行的空间位置 */
    [-] grid-column: ...;
        grid-column-start: ;
        grid-column-end: ;
    /* 项目列的空间位置 */
    [-] grid-row: ...;
        grid-row-start: ;
        grid-row-end: ;

    /* ------------------- */
    /* ----- 表格模型 ----- */
    /* ------------------- */

    /* 表格布局算法 */
    table-layout:    auto | fixed;
    /* 表格空单元格的样式显示处理 */
    empty-cells:     show | hide;
    /* 表格标题位置 */
    caption-side:    top | bottom | block-start | block-end | inline-start | inline-end;
    /* 表格的边框是否合并 */
    border-collapse: collapse | separate;
    /* 设置相邻单元格边框之间的边距 */
    border-spacing:  <length> ;

    /* ------------------- */
    /* ----- 列表盒子 ----- */
    /* ------------------- */

    /* 列表符号 */
    [-] list-style: ...;
        /* 列表符号风格 */
        list-style-type:     none | <counter-style> | <string>;
        /* 列表符号定位 */
        list-style-position: inside | outside;
        /* 指定图片作为列表符号 */
        list-style-image:    none | <url>;

    /* ------------------- */
    /* ----- 标注模型 ----- */
    /* ------------------- */

    /* 注释的对齐方式 */
    ruby-align: start | center | space-between | space-around;
    /* 在一个ruby容器内如何处理多个注释 */
    ruby-merge: auto | collapse | separate;
    /* 注释的放置位置 */
    ruby-position: over | under | inter-character;

    /* ---------------------------- */
    /* ---------- 盒子属性 --------- */
    /* ---------------------------- */

    /* 改变盒模型对元素宽高的计算方式 */
    box-sizing: content-box | border-box;

    /* ------------------- */
    /* ----- 盒子尺寸 ----- */
    /* ------------------- */

    /* 指定了元素内容区的宽度。*/
    width:     <length> | <percentage> | auto | max-content | min-content | fill-available | fit-content;
    /* 为元素设置最小宽度 */
    min-width: <length> | <percentage> | max-content | min-content | fill-available | fit-content;
    /* 为元素设置最大宽度 */
    max-width: none | <length> | <percentage> | max-content | min-content | fill-available | fit-content;

    /* 指定了元素内容区的高度 */
    height:     <length> | <percentage> | auto;
    /* 为元素设置最小高度 */
    min-height: <length> | <percentage> | max-content | min-content | fill-available | fit-content;
    /* 为元素设置最大高度 */
    max-height: none | <length> | <percentage> | max-content | min-content | fill-available | fit-content;

    /* 盒子内边距 */
    [-] padding: ...;
        padding-top:    <length> | <percentage>;
        padding-right:  <length> | <percentage>;
        padding-bottom: <length> | <percentage>;
        padding-left:   <length> | <percentage>;

    /* 盒子边框属性 */
    [-] border: ...;
          /* 边框宽度 */
          [-] border-width: ...;
              border-top-width:    <length> | thin | medium | thick;
              border-right-width:  <length> | thin | medium | thick;
              border-bottom-width: <length> | thin | medium | thick;
              border-left-width:   <length> | thin | medium | thick;
          /* 边框样式*/
          [-] border-style: ...;
              border-top-style:    none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset;
              border-right-style:  none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset;
              border-bottom-style: none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset;
              border-left-style:   none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset;
          /* 边框颜色 */
          [-] border-color: ...;
              border-top-color:    <color>;
              border-right-color:  <color>;
              border-bottom-color: <color>;
              border-left-color:   <color>;
          /* 边框图片属性，会覆盖 border-style */
          [-] border-image: ...;
              /* 图片资源路径 */ 
              border-image-source: none | <url>;
              /* 图像边框的向内偏移 */
              border-image-slice:  <number> | <percentage> | fill;
              /* 边框宽度，会覆盖 border-width 属性 */
              border-image-width:  <length> | <percentage> | <number> | auto;
              /* 边框图像可超出边框盒的大小 */
              border-image-outset: <length> | <number>;
              /* 图片如何填充边框 */
              border-image-repeat: stretch | repeat | round;
          /* 上边框的属性 */
          [-] border-top: ...;
              border-top-width: ;
              border-top-style: ;
              border-top-color: ;
          /* 右边框的属性 */
          [-] border-right: ...;
              border-right-width: ;
              border-right-style: ;
              border-right-color: ;
          /* 下边框的属性 */
          [-] border-bottom: ...;
              border-bottom-width: ;
              border-bottom-style: ;
              border-bottom-color: ;
          /* 左边框的属性 */
          [-] border-left: ...;
              border-left-width: ;
              border-left-style: ;
              border-left-color: ;
    /* 边框圆角 */
    [-] border-radius: ...;
        border-top-right-radius:    <length> | <percentage>;
        border-bottom-right-radius: <length> | <percentage>;
        border-bottom-left-radius:  <length> | <percentage>;
        border-top-left-radius:     <length> | <percentage>;

    /* 盒子轮廓线 */
    [-] outline: ...;
        /* 轮廓线宽度 */
        outline-width: <length> | thin | medium | thick;
        /* 轮廓线颜色 */
        outline-color: <color> | inver;
        /* 轮廓线风格 */
        outline-style: auto | none | dotted | dashed | solid | double | groove | ridge | inset | outset;
    /* 对轮廓进行偏移 */
    outline-offset: <length>;

    /* 为元素声明外边距 */
    [-] margin: ...;
        margin-top:    <length> | <percentage> | auto;
        margin-right:  <length> | <percentage> | auto;
        margin-bottom: <length> | <percentage> | auto;
        margin-left:   <length> | <percentage> | auto;

    /* ------------------- */
    /* ----- 盒子样式 ----- */
    /* ------------------- */

    /* 设置元素前景色 */
    color: <color>;

    /* 声明背景属性 */
    [-] background: ...;
        /* 为元素设置一个或多个背景图像 */
        background-image:      none | <url>;
        /* 背景图片的初始位置 */
        background-position:   left | center | right | top | bottom | <percentage> | <length>;
        /* 设置背景图片大小 */
        background-size:       <length> | <percentage> | auto | cover | contain;
        /* 背景图片平铺方式 */
        background-repeat:     no-repeat | repeat-x | repeat-y | repeat | space | round;
        /* 指定背景图片原点位置的背景相对区域 */
        background-origin:     border-box | padding-box | content-box;
        /* 背景在元素内的覆盖范围 */
        background-clip:       border-box | padding-box | content-box;
        /* 背景是否随跟随容器滚动 */
        background-attachment: fixed | local | scroll;
        /* 背景色 */
        background-color:      <color> | transparent;

    /* 背景图片以及背景色的混合模式 */
    background-blend-mode: <blend-mode>;
    /* 定义元素是否创建新的混合环境 */
    isolation:             auto | isolate;

    /* 对元素进行裁剪 */
    clip-path: url | none | <basic-shape> | <geometry-box>;

    /* 对元素使用遮罩 */
    [-] mask: ...;
        /* 遮罩层图像 */
        mask-image:     none | <url>;
        /* 遮罩层模式 */
        mask-mode:      alpha | luminance | match-source;
        /* 遮罩层位置 */
        mask-position:  <position>;
        /* 遮罩层大小 */
        mask-size:      <length> | <percentage> | auto | cover | contain;
        /* 遮罩层如何重复性 */
        mask-repeat:    repeat-x | repeat-y | repeat | space | round | no-repeat;
        /* 遮罩层的定位区域 */
        mask-origin:    border-box | padding-box | content-box | margin-box | fill-box | stroke-box | view-box;
        /* 遮罩层的影响范围 */
        mask-clip:      border-box | padding-box | content-box | margin-box | fill-box | stroke-box | view-box | no-clip;
        /* 选择遮罩层的叠加方式 */
        mask-composite: add | subtract | intersect | exclude;
    /* <mask>标签中遮罩以亮度或是透明度呈现 */
    mask-type: luminance | alpha;

    /* 滤镜属性 */
    filter: <url> | <filter-function>;

    /* 设置元素投影 */
    box-shadow: inset | <offset-x> <offset-y> | <blur-radius> | <spread-radius> | <color>;

    /* 设置透明度 */
    opacity: <number>;

    /* 隐藏元素并保留空间位置 */
    visibility: visible | hidden | collapse;

    /* ---------------------------- */
    /* ---------- 盒子内容 --------- */
    /* ---------------------------- */

    /* ------------------- */
    /* ----- 溢出处理 ----- */
    /* ------------------- */

    /* 规定了内容溢出容器时的处理 */
    [-] overflow: ...;
        /* 水平溢出的处理 */
        overflow-x: visible | hidden | scroll | auto;
        /* 垂直溢出的处理 */
        overflow-y: visible | hidden | scroll | auto;

    /* ------------------- */
    /* ----- 垂直对齐 ----- */
    /* ------------------- */

    /* 指定行内元素或表格单元格元素的垂直对齐方式 */
    vertical-align: baseline | sub | super | text-top | text-bottom | middle | top | bottom | <percentage> | <length>;

    /* ------------------- */
    /* ----- 内容分列 ----- */
    /* ------------------- */

    /* 设置列属性 */
    [-] columns: ...;
        /* 设置列的宽度 */
        column-width: <length> | auto;
        /* 设置被划分的列数 */
        column-count: <number> | auto;
    /* 声明列的样式 */
    [-] column-rule: ...;
        /* 列之间的宽度 */
        column-rule-width: <length> | thin | medium | thick;
        /* 列之间的分割样式 */
        column-rule-style: none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset;
        /* 列之间的颜色 */
        column-rule-color: <color>;
    /* 声明内容如何分割成列 */
    column-fill: auto | balance;
    /* 规定元素横跨列数 */
    column-span: none | all;
    /* 声明列之间的间隔 */
    column-gap:  <length> | normal;
    /* 指定留在容器底部元素最小行的数量 */
    orphans:     <integer>;

    /* ------------------- */
    /* ----- 文本渲染 ----- */
    /* ------------------- */

    /* ------------- */
    /* -- 排版模式 -- */
    /* ------------- */

    /* 规定文本的排版模式 */
    writing-mode:         horizontal-tb | vertical-rl | vertical-lr | sideways-rl | sideways-lr;
    /* 纵横混排 */
    text-combine-upright: none | all | <integer>;
    /* 双向排列 */
    unicode-bidi:         normal | embed | bidi-override | isolate | isolate-override | plaintext;
    /* 控制字符方向 */
    text-orientation:     mixed | upright | sideways;
    /* 规定文本书写方向 */
    direction:            ltr | rtl;

    /* ------------- */
    /* -- 文本样式 -- */
    /* ------------- */

    /* 定义如何渲染字体 */
    text-rendering: auto | optimizeSpeed | optimizeLegibility | geometricPrecision;

    /* 设置OpenType字体样式集，https://blogs.msdn.microsoft.com/ie_cn/2012/01/17/css-4 */
    font-feature-settings:  normal | <feature-tag-value>;
    /* 声明OpenType文本的语言渲染处理 */
    font-language-override: normal | <string>;

    /* 文本效果样式 */
    [-] font: caption | icon | menu | message-box | small-caption | status-bar | ...;
        /* 选择字体风格 */
        font-style:   normal | italic | oblique;
        /* 西文字体小写转换大写 */
        font-variant: normal | none | small-caps...;
        /* 指定字重 */
        font-weight:  normal | bold｜lighter | bolder | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900;
        /* 对字体进行变形 */
        font-stretch: normal | ultra-condensed | extra-condensed | condensed | semi-condensed | semi-expanded | expanded | extra-expanded | ultra-expanded;
        /* 字体大小 */
        font-size:    <length> | <percentage> | larger | smaller | xx-small | x-small | small | medium | large | x-large | xx-large;
        /* 声明渲染字体 */
        font-family:  <family-name> | <generic-name>;
        /* 设置行高 */
        line-height:  normal | <number> | <length> | <percentage>;

    /* ------------- */
    /* -- 文本控制 -- */
    /* ------------- */

    /* 文本溢出处理 white-space:nowrap; overflow: hidden;*/
    text-overflow: clip | ellipsis | <string>;

    /* 处理元素中的空白符 */
    white-space: normal | pre | nowrap | pre-wrap | pre-line;

    /* 是否允许单词中断换行 */
    overflow-wrap: normal | break-word;
    word-wrap:     normal | break-word;

    /* 声明单词断行规则 */
    word-break: normal | break-all | keep-all;
    /* 声明文本断行规则 */
    line-break: auto | loose | normal | strict;
    /* 西文文本换行时如何处理连字符 */
    hyphens:    none | manual | auto;

    /* 元素内的内容如何对齐 */
    text-align:      start | end | left | right | center | justify | match-parent;
    /* 规定如何对齐末行元素 */
    text-align-last: auto | start | end | left | right | center | justify;
    /* 文本两侧对齐时的空白填充方式 */
    text-justify:    auto | inter-character | inter-word | none;

    /* 字体合成 */
    font-synthesis: none | weight | style;

    /* 定义字体的aspect值（字体的小写字母x的高度与font-size高度之间的比率被称为一个字体的 aspect 值） */
    font-size-adjust: none | <number>;

    /* 定义字间距 */
    letter-spacing: normal | <length>;
    /* 控制西文字符间隙距离 */
    font-kerning:   auto | normal | none;
    /* 声明标签和单词的间距 */
    word-spacing:   normal | <length> | <percentage>;

    /* 控制文本大小写 */
    text-transform: none | capitalize | uppercase | lowercase | full-width;

    /* ------------- */
    /* -- 文本装饰 -- */
    /* ------------- */

    /* 为元素内容添加引用符号 */
    quotes: none | <string>;

    /* 制表符（U+0009）宽度 */
    tab-size: <integer> | <length>;

    /* 文本首行缩进 */
    text-indent: <length> | <percentage> | hanging | each-line;

    /* 文本重点标记 */
    [-] text-emphasis: ...;
        /* 标记符号的类型 */
        text-emphasis-style:    none | open | dot | circle | double-circle | triangle | sesame | <string>;
        /* 标记符号的颜色 */
        text-emphasis-color:    <color>;
        /* 文本重点标记的渲染位置 */
        text-emphasis-position: over | under | right | left;
        
    /* 文本修饰线 */
    [-] text-decoration: ...;
        /* 文本修饰线的颜色 */
        text-decoration-color: <color>;
        /* 文本修饰线的类型 */
        text-decoration-style: solid | double | dotted | dashed | wavy;
        /* 文本修饰线的渲染位置 */
        text-decoration-line:  none | underline | overline | line-through | blink;
    /* 文本下划线位置 */
    text-underline-position: auto | under | left | right | under left | right under;

    /* 文本阴影 */
    text-shadow: none | <color> | <offset-x> <offset-y> | <blur-radius>;

    /* ------------------- */
    /* ----- 图片元素 ----- */
    /* ------------------- */

    /* 定义图片缩放算法 */
    image-rendering:   auto | crisp-edges | pixelated;
    /* 修正图片的预设方向 */
    image-orientation: from-image | <angle> | flip;
    /* 设定图片分辨率 */
    image-resolution:  <resolution>;

    /* 设定alpha值提取图像形状 */
    shape-image-threshold: <number>;
    /* 为形状添加轮廓 */
    shape-outside:         none | <shape-box> | <basic-shape> | <url>;
    /* 为形状添加外边距 */
    shape-margin:          <length> | <percentage>;


    /* ------------------------------------------------ */
    /* -------------------- 盒子变形 ------------------- */
    /* ------------------------------------------------ */

    /* 子元素空间状态（2d/3d）*/
    transform-style:  flat | preserve-3d;
    /* 元素变形 */
    transform:        none | <transform-function>;
    /* 元素变形范围 */
    transform-box:    border-box | fill-box | view-box;
    /* 元素变形的中心点*/
    transform-origin: <percentage> | <length> | left | center | right | top | bottom | center;

    /* 设置透视的观测距离 */
    perspective:        none | <length>;
    /* 设置透视的灭点位置 */
    perspective-origin: <x-position> | <y-position> | <percentage> | <length>;

    /* 3d状态下，声明元素背面是否可见 */
    backface-visibility: visible | hidden;

    /* ------------------------------------------------ */
    /* -------------------- 动态效果 ------------------- */
    /* ------------------------------------------------ */

    /* ---------------------------- */
    /* ---------- 过渡动画 --------- */
    /* ---------------------------- */

    /* 定义元素过渡效果 */
    [-] transition: none | ...;
        /* 指定需过渡的属性 */
        transition-property:        none | all | <transition-ident>;
        /* 过渡效果执行时间 */
        transition-duration:        <time>;
        /* 定义过渡缓动函数 */
        transition-timing-function: <timing-function>;
        /* 延迟过渡 */
        transition-delay:           <time>;

    /* 动画属性 */
    [-] animation: ...;
        /* 指定应用声明过的动画标识 */
        animation-name:            none | <animation-ident>;
        /* 指定动画执行周期 */
        animation-duration:        <time>;
        /* 定义动画缓动函数 */
        animation-timing-function: <timing-function>;
        /* 定义延时 */
        animation-delay:           <time>;
        /* 定义动画循环次数 */
        animation-iteration-count: infinite | <number>;
        /* 指示是否反向播放 */
        animation-direction:       normal | reverse | alternate | alternate-reverse;
        /* 指定动画执行前后的元素样式 */
        animation-fill-mode:       none | forwards | backwards | both;
        /* 定义或查询一个动画的当前状态 */
        animation-play-state:      running | paused;

    /* ---------------------------- */
    /* ---------- 滚动效果 --------- */
    /* ---------------------------- */

    /* 导航或者CSSOM api产生滚动的过渡效果 */
    scroll-behavior:         auto | smooth;
    /* 定义元素滚动的snap点类型 */
    scroll-snap-type:        none | mandatory | proximity;
    /* 定义元素滚动的snap点坐标位置*/
    scroll-snap-destination: <position>;
    /* 定义元素滚动的snap点坐标偏移位置 */
    scroll-snap-coordinate:  none | <position>;

    /* ------------------------------------------------ */
    /* -------------------- 其他属性 ------------------- */
    /* ------------------------------------------------ */

    /* ---------------------------- */
    /* ---------- 用户行为 --------- */
    /* ---------------------------- */

    /* 是否可由用户调整元素的尺寸 */
    resize: none | both | horizontal | vertical;

    /* 声明鼠标悬浮样式 */
    cursor:   <url> | auto | default | none | context-menu | help | pointer | progress | wait | cell | crosshair | text | vertical-text | alias | copy | move | no-drop | not-allowed | e-resize | n-resize | ne-resize | nw-resize | s-resize | se-resize | sw-resize | w-resize | ew-resize | ns-resize | nesw-resize | nwse-resize | col-resize | row-resize | all-scroll | -zoom-in | -zoom-out | grab | grabbing;

    /* 规定用户手势操作方式 */
    touch-action: auto | none | pan-x | pan-left | pan-right | pan-y | pan-up | pan-down | pinch-zoom | manipulation;

    /* 声明插入光标的颜色 */
    caret-color: auto | <color>;
    /* 是否允许激活输入法（IME）状态 */
    ime-mode:    auto | normal | active | inactive | disabled;

    /* ---------------------------- */
    /* ---------- 元素属性 --------- */
    /* ---------------------------- */

    /* 替换元素的内容如何适应容器 */
    object-fit:      fill | contain | cover | none | scale-down;
    /* 确定替换元素的位置 */
    object-position: left | center | right | top | bottom | <length> | <percentage>;

    /* 在::before和::after中插入内容*/
    content: none | normal | <string> | <uri> | <counter> | attr() | open-quote | close-quote | no-open-quote | no-close-quote;

    /* 为计数器设置初始值 */
    counter-reset:     <custom-ident> <integer> | none;
    /* 为元素添加计数器 */
    counter-increment: <custom-ident> <integer> | none;


     /* 通知浏览器进行元素动效的优化 */
    will-change: auto | scroll-position | contents | <custom-ident>;

    /* 设置鼠标事件穿透 */
    pointer-events: auto | none | visiblePainted | visibleFill | visibleStroke | visible | painted | fill | stroke | all | inherit;

    /* 声明元素重叠时显示的权重 */
    z-index: <integer> | auto;

     /* 重置除了 unicode-bidi 和 direction 之外的所有属性至初始值或继承值 */
    all: initial | inherit | unset;

    /* ---------------------------- */
    /* ---------- 定义变量 --------- */
    /* ---------------------------- */

    /* 自定义属性 */
    --*: ...;

    /* ---------------------------- */
    /* ---------- 页面打印 --------- */
    /* ---------------------------- */

    /* 设置元素之前的分页符 */
    page-break-before: auto | always | avoid | left | right;
    /* 设置元素之后的分页符 */
    page-break-after:  auto | always | avoid | left | right;
    /* 设置元素容器内的分页符 */
    page-break-inside: auto | avoid;

    /* 页面打印时分页保留的最少行数 */
    widows: <integer>;

}

```  
[↑ top](#note-css-order)