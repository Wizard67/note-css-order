# note-css-order
> css 属性书写顺序推荐，根据 [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS) 归纳整理。  
> 需要查询完整的规范内容？[Selectors Level 4](https://drafts.csswg.org/selectors-4/)


## summary  

###  Pseudo-classes 伪类
``` css

    /* Logical Combinations */
    :any()                  /* 匹配 集合内指定 的元素 */
    :not(selector)          /* 排除 指定选择器 的元素 */

    /* Linguistic Pseudo-classes */
    :dir(ltr|rtl)           /* 匹配 设置dir(文字书写方向)属性 的元素 */
    :lang(language-code)    /* 匹配 设置lang(定义元素语言)属性 的元素 */

    /* Location Pseudo-classes */
    :link                   /* 匹配 未处于访问记录中 的链接 */
    :visited                /* 匹配 处于访问记录中 的链接 */
    :target                 /* 匹配 URL指向的锚点 的元素 */
    :scope                  /* 匹配 设置scoped属性的style标签 的作用域 */

    /* User Action Pseudo-classes */
    :hover                  /* 匹配 处于鼠标悬停 的元素 */
    :active                 /* 匹配 处于激活状态 的元素 */
    :focus                  /* 匹配 处于聚焦状态 的元素 */

    /* The Input Pseudo-classes */
    :enabled                /* 匹配 可以编辑 的元素 */
    :disabled               /* 匹配 禁止编辑 的元素 */
    :read-only              /* 匹配 内容只读 的元素 */
    :read-write             /* 匹配 内容可编辑 的元素 */
    :default                /* 匹配 页面载入默认选中 的元素 */
    :checked                /* 匹配 选中状态 的元素 */
    :indeterminate          /* 匹配 模糊状态 的元素 */
    :valid                  /* 匹配 输入内容通过类型验证 的元素 */
    :invalid                /* 匹配 输入内容无法通过类型验证 的元素 */
    :in-range               /* 匹配 输入数值符合范围 的元素 */
    :out-of-range           /* 匹配 输入数值溢出范围 的元素 */
    :required               /* 匹配 设置必填属性 的元素 */
    :optional               /* 匹配 可选字段 的元素 */

    /* Tree-Structural pseudo-classes */
    :root                   /* 匹配 文档树 的根元素*/
    :empty                  /* 匹配 无子节点 的元素 */
    
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