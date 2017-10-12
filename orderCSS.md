# note-css-order
> CSS 伪类、伪元素、规则、以及属性的速查列表，根据 [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS) 归纳整理。  

* [Pseudo-classes 伪类]()
* [Pseudo-elements 伪元素]()
* [At-rule 规则]()
* [Properties 属性]()

###  Pseudo-classes 伪类
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

``` css



```