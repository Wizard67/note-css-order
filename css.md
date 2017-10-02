```css

<length>: .em | .ex | .ch | .rem | .vh | .vw | .wmin | .vmax | .px | .mm | .cm | .in | .pt | .pc | [.mozmm];
<percentages>: .%;
<image>: url();
<color>: <hex-color> | <named-color> | transparent | currentcolor | <rgb()> | <hsl()> | <rgba()> | <hsla()> | <deprecated-system-color>;
<shape>: rect(<top>, <right>, <bottom>, <left>);
<time>: .ms | .s;


div {
  /*/设置元素的定位方式，为元素定义定位规则。*/
  position: static | relative | relative | fixed | *sticky;
  /*->!position:static，使定位元素产生位置偏移*/
  top: <length> | <percentages> | auto;
  right: <length> | <percentages> | auto;
  bottom: <length> | <percentages> | auto;
  left: <length> | <percentages> | auto;

	/*使一个元素脱离正常的文档流，然后被安放到它所在容器的的左端或者右端，并且其他的文本和行内元素围绕它安放。*/
	float: none | left | right;
	/*是否清除浮动*/
	clear: none | left | right | both | *inline-start | *inline-end;


  /*指定元素渲染出来的盒类型*/
  display: none | inline | block | inline-block | flex | list-item | table~;
	  /*->display:flex，创建可伸缩项目*/
	  flex: ;
	    /*定义弹性盒子的拉伸因子*/
	    flex-grow: <number>;
	    /*定义弹性盒子的收缩规则*/
	    flex-shrink: <number>;
	    /*指定 flex item 在主轴方向的初始大小*/
	    flex-basis: <length> | <percentages | *content;
	  /*规定了弹性容器中的可伸缩项目在布局时的顺序*/
	  order: <integer>;
	  /*指定了内部元素是如何在flex容器中布局的，定义了主轴的方向*/
	  flex-direction: row | row-reverse | column | column-reverse;
	  /*描述了 flex 条目行的是被强制放在一行中或者是被放在多个行上*/
	  flex-flow: nowrap | wrap | wrap-reverse;
	  /*定义了浏览器如何分配顺着父容器主轴的弹性 flex 元素之间及其周围的空间*/
	  justify-content: flex-start | flex-end | center | space-between | space-around;

	  [fix]/* 声明如何分配多行弹性容器中侧轴的空间位置 */
	  align-content: flex-start | flex-end | center | space-between | space-around | stretch;
      
	  [fix]/* 声明弹性容器中侧轴上项目的对齐方式 */
	  align-items: flex-start | flex-end | center | baseline | stretch;

	  [fix]/* 单独声明项目在弹性容器侧轴上的对齐方式 */
	  align-self: auto | flex-start | flex-end | center | baseline | stretch;

	  /*->table ,定义了表格布局算法*/
	  table-layout: auto | fixed;
	  /*->table ,隐藏表格中空单元格上的边框和背景*/
	  empty-cells: show | hide;
	  /*规定表格标题放置位置*/
	  caption-side: top | bottom | *left | *right | *top-outside | *bottom-outside;
	  /*->table ,决定表格的边框是分开的还是合并*/
	  border-collapse: collapse | separate;
	  /*->table ,设置相邻单元格之间的边距*/
	  border-spacing: <length> ;

	  /*->dispaly:list-item，设置列表符号*/
 		list-style: ;
	    /*列表符号外观*/
	    list-style-type: none | <counter-style> | <string>;
	    /*列表符号定位*/
	    list-style-position: inside | outside;
	    /*指定图片作为列表符号*/
	    list-style-image: none | <image>;


  /*改变默认的 CSS 盒模型 对元素宽高的计算方式*/
  box-sizing: content-box | border-box;
	  /*属性指定了元素内容区的宽度。*/
	  width: <length> | <percentage> | auto | -max-content | -min-content | -fill-available | -fit-content;
	  /*属性为给定元素设置最小宽度。*/
	  min-width: <length> | <percentage> | -max-content | -min-content | -fill-available | -fit-content;
	  /*属性用来给元素内容区设置最大宽度值。*/
	  max-width: none | <length> | <percentage> | -max-content | -min-content | -fill-available | -fit-content;

	  /*属性指定了元素内容区的高度。*/
	  height: <length> | <percentage> | auto;
	  /*属性为给定元素设置最小高度。*/
	  min-height: <length> | <percentage> | -max-content | -min-content | -fill-available | -fit-content;
	  /*属性用来给元素内容区设置最大高度值。*/
	  max-height: none | <length> | <percentage> | -max-content | -min-content | -fill-available | -fit-content;

	  /*属性为元素声明内边距*/
	  padding: <length> | <percentage> (1,4);
	    padding-top: ;
	    padding-right: ;
	    padding-bottom: ;
	    padding-left: ;

	  [fix]/* 声明边界属性 */
	  [-] border: ;
	    /*声明统一边框宽度*/
	    [-] border-width: <length> | thin | medium | thick;
	      border-top-width: ;
	      border-right-width: ;
	      border-bottom-width: ;
	      border-left-width: ;
	    /*声明统一边框样式*/
	    [-] border-style: none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outse;
	      border-top-style: ;
	      border-right-style: ;
	      border-bottom-style: ;
	      border-left-style: ;
	    /*声明统一边框颜色*/
	    [-] border-color: <color>;
	      border-top-color: ;
	      border-right-color: ;
	      border-bottom-color: ;
	      border-left-color: ;
	    /*声明统一边框图片样式，会覆盖 border-style，简写值为 none*/
	    [-] border-image:;
	      /*定义图片存放路径*/
	      border-image-source: none | <image> | -<linear-gradient()>;
	      /*规定图像边框的向内偏移*/
	      border-image-slice: <number> | <percentage> | fill;
	      /*定义边框宽度，会覆盖 border-width 属性*/
	      border-image-width: <length> | <percentage> | <number> | auto;
	      /*属性定义边框图像可超出边框盒的大小*/
	      border-image-outset: <length> | <number>;
	      /*定义图片如何填充边框*/
	      border-image-repeat: stretch | repeat | round;
	    /*简写上边框的所有属性*/
	    [-] border-top: ;
	      border-top-width: ;
	      border-top-style: ;
	      border-top-color: ;
	    /*简写右边框的所有属性*/
	    [-] border-right: ;
	      border-right-width: ;
	      border-right-style: ;
	      border-right-color: ;
	    /*简写下边框的所有属性*/
	    [-] border-bottom: ;
	      border-bottom-width: ;
	      border-bottom-style: ;
	      border-bottom-color: ;
	    /*简写左边框的所有属性*/
	    [-] border-left: ;
	      border-left-width: ;
	      border-left-style: ;
	      border-left-color: ;
	  /*设置边框圆角，可影响 background*/
	  [-] border-radius: <length> | <percentage> (1,4 : 1/.);
	    border-top-right-radius: ;
	    border-bottom-right-radius: ;
	    border-bottom-left-radius: ;
	    border-top-left-radius: ;

	  /*为元素设置一个或多个独立的轮廓*/
	  outline: ;
	    /*设置轮廓宽度*/
	    outline-width: thin | medium | thick | <length>;
	    /*为轮廓设置颜色*/
	    outline-color: <color> | inver;
	    /*为轮廓设置样式*/
	    outline-style: auto | none | dotted | dashed | solid | double | groove | ridge | inset | outset;
	  /*对轮廓进行偏移，并在边框边缘进行绘制*/
	  outline-offset: <length>;

	  /*属性为元素声明外边距*/
	  margin: <-length> | <percentage> | auto (1,4);
	    margin-top: ;
	    margin-right: ;
	    margin-bottom: ;
	    margin-left: ;

	  [fix]/* 声明背景属性 */
	  [-] background: ;
	    /* 为元素设置一个或多个背景图像 */
	    background-image: none | <image>;
	    /* 背景图片的初始位置 */
	    background-position: left | center | right | top | bottom | <percentage> | <length>;
	    /* 设置背景图片大小 */
	    background-size: <length> | <percentage> | auto | cover | contain;
	    /* 背景图片平铺方式 */
	    background-repeat: no-repeat | repeat-x | repeat-y | repeat | space | round;
	    /* 指定背景图片原点位置的背景相对区域 */
	    background-origin: border-box | padding-box | content-box;
	    /* 背景在元素内的覆盖范围 */
	    background-clip: border-box | padding-box | content-box;
	    /* 背景是否随跟随容器滚动 */
	    background-attachment: fixed | local | scroll;
	    /* 背景色 */
	    background-color: <color> | transparent;

	  [fix] /* 背景图片以及背景色的混合模式 */
	  background-blend-mode: <blend-mode>;

	  /*描述一个或多个阴影效果，可受 border-radius 影响*/
	  box-shadow: inset | <offset-x> <offset-y> | <blur-radius> | <spread-radius> | <color>;

	  /*指定了一个元素的透明度*/
	  opacity: <number>;
	  /*滤镜属性*/
	  -filter: <filter-function> (1,n);


  /*设置列属性*/
  columns: ;
    /*设置列的宽度*/
    -column-width: <length> | auto;
    /*设置被划分的列数*/
    -column-count: <integer> | auto;
  /*设置元素列之间的间隔大小*/
  -column-gap: <length> | normal;
  /*列之间的宽度、样式和颜色*/
  -column-rule: ;
    /*设置列之间的宽度*/
    -column-rule-width: <length> | thin | medium | thick;
    /*设置列之间的分割样式*/
    -column-rule-style: none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset;
    /*设置列之间的颜色*/
    -column-rule-color: <color>;
  /*规定元素横跨多少列*/
  -column-span: none | all;
  /*指定留在页面底部元素最小行的数量*/
  orphans: <integer>;


  /*规定了内容元素溢出时的处理*/
  overflow: visible | hidden | scroll | auto;
    /*水平溢出的处理*/
    overflow-x: visible | hidden | scroll | auto;
    /*垂直溢出的处理*/
    overflow-y: visible | hidden | scroll | auto;


  /*指定行内元素或表格单元格元素的垂直对齐方式*/
  vertical-align: baseline | sub | super | text-top | text-bottom | middle | top | bottom | <percentage> | -<length>;



  /*定义如何渲染字体*/
  text-rendering: auto | optimizeSpeed | optimizeLegibility | geometricPrecision;

	  /*规定文本的排版模式*/
	  -writing-mode: horizontal-tb | vertical-rl | vertical-lr | sideways-rl | sideways-lr;
	  /*->writing-mode:^horizontal-tb，纵横混排*/
	  -text-combine-upright: none | all | digits <integer>;
	  /*->writing-mode:^horizontal-tb，控制字符方向*/
	  *text-orientation: mixed | upright | sideways;
	  /*规定文本书写方向*/
	  direction: ltr | rtl;
	  /*双向排列*/
	  unicode-bidi: normal | embed | bidi-override | -isolate | *isolate-override | *plaintext;

	  /*文字效果样式*/
	  font: ;
	    /*选择字体的斜体样式*/
	    font-style: normal | italic | oblique;
	    /*英文字体小写转换大写*/
	    font-variant: small-caps | ...;
	    /*指定了字体的粗细程度*/
	    font-weight: normal | bold｜lighter | bolder | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900;
	    /*对字体进行拉伸*/
	    *font-stretch: normal | ultra-condensed | extra-condensed | condensed | semi-condensed | semi-expanded | expanded | extra-expanded | ultra-expanded;
	    /*定义字体大小*/
	    font-size: <length> | <percentage> | larger | smaller | xx-small | x-small | small | medium | large | x-large | xx-large;
	    /*由字体名或者字体族名组成的列表来为选定的元素设置字体*/
	    font-family: <family-name> | <generic-name>;
	    /*指定 line-box 的高度*/
	    line-height: normal | <number> | <length> | <percentage>;

	  /*为元素的文本设置前景色*/
	  color: <color>;

	  /*设置open type 字体样式集，https://blogs.msdn.microsoft.com/ie_cn/2012/01/17/css-4*/
	  -font-feature-settings: normal | <feature-tag-value>;

	  /*如何处理元素中的空白符*/
	  white-space: normal | pre | nowrap | pre-wrap | pre-line;
	  /*->white-space:nowrap; overflow: hidden;文本溢出处理*/
	  text-overflow: clip | ellipsis | *<string>;

	  /*定义字间距*/
	  letter-spacing: normal | <length>;

	  /*控制英文字符间的空白*/
	  font-kerning: auto | normal | none;
	  /*声明标签和单词的间距*/
	  word-spacing: normal | <length> | <percentage>;
	  /*控制文本的大小写*/
	  text-transform: none | capitalize | uppercase | lowercase;
	  /*是否允许单词中断换行*/
	  overflow-wrap ( word-wrap ): normal | break-word;
	  /*指定怎样在单词内断行*/
	  word-break: normal | break-all | keep-all;
	  /*告知浏览器在换行时如何使用连字符连接单词*/
	  -hyphens: none | manual | auto;

	  /*定义行内内容如何相对其块父级元素对齐*/
	  text-align: left | right | center | justify | *start | *end | *<string> | *match-parent;
	  /*规定如何对齐最后一行*/
	  text-align-last: left | right | center | justify | auto | *start | *end;

	  /*设置引用符号*/
	  quotes: none | <string>;
	  /*自定义制表符 (U+0009) 的宽度*/
	  tab-size: <integer> | <length>;
	  /*首行文本缩进*/
	  text-indent: <length> | <percentage> | *hanging | *each-line;
	  /*文本进行重点标记*/
	  -text-emphasis: ;
	    -text-emphasis-color: <color>;
	    -text-emphasis-position: over | under | *right | *left (1,2);
	    -text-emphasis-style: none | open | dot | circle | double-circle | triangle | sesame | <string>;
	  /*文本渲染修饰（下划线、顶划线、删除线）*/
	  text-decoration: none | underline | overline | line-through | blink (1,4);
	    *text-decoration-color: <color>;
	    *text-decoration-style: solid | double | dotted | dashed | wavy;
	    *text-decoration-line: none | underline | overline | line-through | blink;
	  /*定义下划线位置*/
	  *text-underline-position: auto | under | left | right | under left | right under;
	  /*为文字添加阴影*/
	  text-shadow: <color> | <offset-x> <offset-y> | <blur-radius>;


  /*定义图片缩放算法*/
  *image-rendering: auto | crisp-edges | pixelated;
  /*修正图片的预设方向*/
  *image-orientation: from-image | <angle> | flip;


  /*指定替换元素的内容应该如何适应容器*/
  object-fit: fill | contain | cover | none | scale-down;
  /*确定替换元素的位置*/
  object-position: left | center | right | top | bottom | <length> | <percentage>;

  /*当元素之间重叠的时候，决定哪一个元素覆盖在其余元素的上方显示。*/
  z-index: <-integer> | auto;
  /*设置元素的缩放*/
  *zoom: auto | <number> | <percentage>;
  /*—>position:absolute，对元素进行裁剪*/
  clip: <shape> | auto;
	/*是否可由用户调整元素的尺寸*/
	resize: none | both | horizontal | vertical | block | inline;
  /*定义鼠标悬浮手势*/
  cursor: auto | default | none | *context-menu | help | pointer | progress | wait | cell | crosshair | text | vertical-text | alias | copy | move | no-drop | not-allowed | e-resize | n-resize | ne-resize | nw-resize | s-resize | se-resize | sw-resize | w-resize | ew-resize | ns-resize | nesw-resize | nwse-resize | col-resize | row-resize | all-scroll | -zoom-in | -zoom-out | *grab | *grabbing | *<image>;
  /*隐藏元素，并将其所占空间用空白占位*/
  visibility: visible | hidden | collapse;

  /*计数器设置初始值*/
  counter-reset: <custom-ident> <integer> | none;
   /*对元素进行编号*/
  counter-increment: <custom-ident> <integer> | none;
  /*->*:before|*:after；用于在元素的  ::before 和 ::after 伪元素中插入内容*/
  content: none | normal | <string> | <image> | <counter> | <attr()> | open-quote | close-quote | no-open-quote | no-close-quote;

  /*为将要改变的元素提前做优化准备工作*/
  *will-change: auto | scroll-position | contents | <custom-ident>;
  /*让元素事件不被鼠标捕获*/
  pointer-events: auto | none;

  [fix] /* 重置除了 unicode-bidi 和 direction 之外的所有属性至初始值或继承值 */
  all: initial | inherit | unset;

  /*设置元素表现样式*/
  -appearance：auto | none;
  /*指定子元素空间状态（2d/3d）*/
  -transform-style: flat | preserve-3d;

  /*模型变形*/
  -transform: none | <transform-function>;
  /*模型 transform 参考*/
  *transform-box: border-box | fill-box | view-box;
  /*更改元素变形的原点*/
  -transform-origin: <percentage> | <length> | left | center | right | top | bottom | center (1,3)

  /*属性指定了观察者与z=0平面的距离，使具有三维位置变换的元素产生透视效果*/
  perspective: none | <length>;
  /*指定了观察者的位置，在属性perspective中被用作消失点*/
  perspective-origin: <x-position> | <y-position> | <percentage> | <length> (1,2);

  [fix]/* 3d状态下，声明元素背面是否可见 */
  backface-visibility: visible | hidden;


  /*定义元素之间的过渡*/
  -transition: ;
    /*延迟过渡*/
    -transition-delay: -<time>;
    /*过渡效果执行时间*/
    -transition-duration: <time>;
    /*指定应用过渡属性*/
    -transition-property: none | all | *<transition-ident>;
    /*定义过渡到缓动函数*/
    transition-timing-function: <timing-function>;


  [fix]/* 动画属性 */
  [-] animation: ;
    /* 指定应用声明过的动画标识 */
    animation-name: none | <animation-ident>;
    /* 指定动画执行周期 */
    animation-duration: <time>;
    /* 定义动画缓动函数 */
    animation-timing-function: <timing-function>;
    /* 定义延时 */
    animation-delay: <time>;
    /* 定义动画循环次数 */
    animation-iteration-count: infinite | <number>;
    /* 指示是否反向播放 */
    animation-direction: normal | reverse | alternate | alternate-reverse;
    /* 指定动画执行前后的元素样式 */
    animation-fill-mode: none | forwards | backwards | both;
    /* 定义或查询一个动画的当前状态 */
    animation-play-state: running | paused;
}


```