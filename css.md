```css

<length>: .em | .ex | .ch | .rem | .vh | .vw | .wmin | .vmax | .px | .mm | .cm | .in | .pt | .pc | [.mozmm];
<percentages>: .%;
<image>: url();
<color>: <hex-color> | <named-color> | transparent | currentcolor | <rgb()> | <hsl()> | <rgba()> | <hsla()> | <deprecated-system-color>;
<shape>: rect(<top>, <right>, <bottom>, <left>);
<time>: .ms | .s;


div {
  [fix]/* 设置元素的定位方式 */
  position: static | relative | absolute | fixed | sticky;
  [fix]/* 使定位后的元素产生位置偏移 */
  top: <length> | <percentages> | auto;
  right: <length> | <percentages> | auto;
  bottom: <length> | <percentages> | auto;
  left: <length> | <percentages> | auto;

	[fix]/* 元素浮动 */
	float: left | right | none | inline-start | inline-end;
	[fix]/* 是否清除浮动 */
	clear: none | left | right | both | inline-start | inline-end;

  [fix]/* 描述元素的盒子类型 */
  display: none | inline | block | list-item | inline-list-item | inline-block | inline-table | table | table-cell | table-column | table-column-group | table-footer-group | table-header-group | table-row | table-row-group | flex | inline-flex | grid | inline-grid | run-in | ruby | ruby-base | ruby-text | ruby-base-container | ruby-text-container | contents;

	[fix]/* 声明项目的空间分配 */
	[-] flex: auto | initial | none | ...;
	  [fix]/* 定义项目的拉伸因子 */
	  flex-grow: <number>;
	  [fix]/* 定义项目的收缩规则 */
	  flex-shrink: <number>;
	  [fix]/* 指定项目在主轴方向的初始大小 */
	  flex-basis: <length> | <percentages> | content;
	[fix]/* 声明容器的主轴方向和换行规则 */
	[-] flex-flow: ...;
		[fix]/* 定义主轴的方向 */
		flex-direction: row | row-reverse | column | column-reverse;
		[fix]/* 声明是否允许换行 */
		flex-wrap: nowrap | wrap | wrap-reverse;
	[fix]/* 声明项目在主轴上的位置和空间分配 */
	justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
	[fix]/* 声明如何分配多行弹性容器中侧轴的空间位置 */
	align-content: flex-start | flex-end | center | space-between | space-around | stretch;
	[fix]/* 声明项目在侧轴上的位置和空间分配 */
	align-items: flex-start | flex-end | center | baseline | stretch;
	[fix]/* 单独声明项目在弹性容器侧轴上的对齐方式 */
	align-self: auto | flex-start | flex-end | center | baseline | stretch;
	[fix]/* 项目在弹性容器中的排序权重 */
	order: <integer>;


	[fix]/* 声明网格布局属性 */
	[-] grid: ...;
		[fix]/**/
		grid-template-rows: ;
		[fix]/**/
		grid-template-columns: ;
		[fix]/**/
		grid-template-areas: ;
		[fix]/**/
		grid-auto-rows: ;
		[fix]/**/
		grid-auto-columns:  ;
		[fix]/**/
		grid-auto-flow:  ;
		[fix]/**/
		grid-column-gap:  ;
		[fix]/**/
		grid-row-gap: ;

	[fix]/* */
	[-] grid-area: ...;
		[fix]/**/
		grid-row-start: ;
		[fix]/**/
		grid-column-start: ;
		[fix]/**/
		grid-row-end: ;	
		[fix]/**/
		grid-column-end: ;

	[fix]/* */
	[-] grid-column: ...;
		[fix]/**/
		grid-column-start: ;
		[fix]/**/
		grid-column-end: ;

	[fix]/* */
	[-] grid-gap: ...;
		[fix]/**/
		grid-row-gap: ;
		[fix]/**/
		grid-column-gap: ;

	[fix]/* */
	[-] grid-row: ...;
		[fix]/**/
		grid-row-start: ;
		[fix]/**/
		grid-row-end: ;

	[fix]/* */
	[-] grid-template: ...;
		[fix]/**/
		grid-template-rows: ;
		[fix]/**/
		grid-template-columns: ;
		[fix]/**/
		grid-template-areas: ;
	
	/*->table ,定义了表格布局算法*/
	table-layout: auto | fixed;
	[fix]/* 表格空单元格的样式显示处理 */
	empty-cells: show | hide;
	[fix]/* 规定表格标题放置位置 */
	caption-side: top | bottom | block-start | block-end | inline-start | inline-end;
	[fix]/* 声明表格的边框是分隔还是合并 */
	border-collapse: collapse | separate;
	[fix]/* 设置相邻单元格边框之间的边距 */
	border-spacing: <length> ;

	[fix]/* 设置列表符号 */
 	[-] list-style: ...;
	  [fix]/* 列表符号风格 */
	  list-style-type: none | <counter-style> | <string>;
	  [fix]/* 列表符号定位 */
	  list-style-position: inside | outside;
	  [fix]/* 指定图片作为列表符号 */
	  list-style-image: none | <url>;


  [fix]/* 改变默认的CSS盒模型对元素宽高的计算方式 */
  box-sizing: content-box | border-box;
	/*属性指定了元素内容区的宽度。*/
	width: <length> | <percentage> | auto | -max-content | -min-content | -fill-available | -fit-content;
	[fix] /* 为元素设置最小宽度 */
	min-width: <length> | <percentage> | max-content | min-content | fill-available | fit-content;
	[fix]/* 为元素内容区设置最大宽度值 */
	max-width: none | <length> | <percentage> | max-content | min-content | fill-available | fit-content;

	[fix]/* 指定了元素内容区的高度 */
	height: <length> | <percentage> | auto;
	[fix]/* 为元素设置最小高度 */
	min-height: <length> | <percentage> | max-content | min-content | fill-available | fit-content;
	[fix]/* 为元素内容区设置最大高度值 */
	max-height: none | <length> | <percentage> | max-content | min-content | fill-available | fit-content;

	[fix]/* 为元素声明内边距 */
	[-] padding: <length> | <percentage>;
	  padding-top: ;
	  padding-right: ;
	  padding-bottom: ;
	  padding-left: ;

	[fix]/* 声明边框属性 */
	[-] border: ...;
	    /* 声明边框宽度 */
	    [-] border-width: <length> | thin | medium | thick;
	      border-top-width: ;
	      border-right-width: ;
	      border-bottom-width: ;
	      border-left-width: ;
	    /* 声明边框样式*/
	    [-] border-style: none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset;
	      border-top-style: ;
	      border-right-style: ;
	      border-bottom-style: ;
	      border-left-style: ;
	    /* 声明边框颜色 */
	    [-] border-color: <color>;
	      border-top-color: ;
	      border-right-color: ;
	      border-bottom-color: ;
	      border-left-color: ;
	    /* 声明边框图片样式，会覆盖 border-style */
	    [-] border-image: ;
	      /* 图片资源路径 */ 
	      border-image-source: none | <image>;
	      /* 图像边框的向内偏移 */
	      border-image-slice: <number> | <percentage> | fill;
	      /* 边框宽度，会覆盖 border-width 属性 */
	      border-image-width: <length> | <percentage> | <number> | auto;
	      /* 边框图像可超出边框盒的大小 */
	      border-image-outset: <length> | <number>;
	      /* 图片如何填充边框 */
	      border-image-repeat: stretch | repeat | round;
	    /* 声明上边框的属性 */
	    [-] border-top: ;
	      border-top-width: ;
	      border-top-style: ;
	      border-top-color: ;
	    /* 声明右边框的属性 */
	    [-] border-right: ;
	      border-right-width: ;
	      border-right-style: ;
	      border-right-color: ;
	    /* 声明下边框的属性 */
	    [-] border-bottom: ;
	      border-bottom-width: ;
	      border-bottom-style: ;
	      border-bottom-color: ;
	    /* 声明左边框的属性 */
	    [-] border-left: ;
	      border-left-width: ;
	      border-left-style: ;
	      border-left-color: ;
	/* 设置边框圆角 */
	[-] border-radius: <length> | <percentage>;
	    border-top-right-radius: ;
	    border-bottom-right-radius: ;
	    border-bottom-left-radius: ;
	    border-top-left-radius: ;

	[fix]/* 为元素设置轮廓线 */
	[-] outline: ...;
	  [fix]/* 设置轮廓线宽度 */
	  outline-width: <length> | thin | medium | thick;
	  [fix]/* 为轮廓线设置颜色 */
	  outline-color: <color> | inver;
	  [fix]/* 轮廓线风格 */
	  outline-style: auto | none | dotted | dashed | solid | double | groove | ridge | inset | outset;
	[fix]/* 对轮廓进行偏移 */
	outline-offset: <length>;

	[fix]/* 为元素声明外边距 */
	[-] margin: <length> | <percentage> | auto;
	  margin-top: ;
	  margin-right: ;
	  margin-bottom: ;
	  margin-left: ;

	[fix]/* 声明背景属性 */
	[-] background: ...;
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

	[fix]/* 背景图片以及背景色的混合模式 */
	background-blend-mode: <blend-mode>;
	[fix]/* 定义元素是否创建新的混合环境 */
	isolation: auto | isolate;

	[fix]/* 设置元素投影 */
	box-shadow: inset | <offset-x> <offset-y> | <blur-radius> | <spread-radius> | <color>;

	[fix] /* 设置透明度 */
	opacity: <number>;
	[fix]/* 滤镜属性 */
	filter: <url> | <filter-function>;


  [fix]/* 设置列属性 */
  [-] columns: ...;
    /* 设置列的宽度 */
    column-width: <length> | auto;
    /* 设置被划分的列数 */
    column-count: <number> | auto;
  [fix]/* 声明列之间的间隔 */
  column-gap: <length> | normal;
  [fix]/* 声明列的样式 */
  [-] column-rule: ...;
    /* 列之间的宽度 */
    column-rule-width: <length> | thin | medium | thick;
    /* 列之间的分割样式 */
    column-rule-style: none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset;
    /* 列之间的颜色 */
    column-rule-color: <color>;
  [fix]/* 规定元素横跨列数 */
  column-span: none | all;
  [fix]/* 指定留在容器底部元素最小行的数量 */
  orphans: <integer>;
	[fix]/* 声明内容如何分割成列 */
	column-fill: auto | balance;


  [fix]/* 规定了内容溢出容器时的处理 */
  overflow: ...;
    [fix]/* 水平溢出的处理 */
    overflow-x: visible | hidden | scroll | auto;
    [fix]/* 垂直溢出的处理 */
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
	  [fix]/* 规定文本书写方向 */
	  direction: ltr | rtl;
	  /*双向排列*/
	  unicode-bidi: normal | embed | bidi-override | -isolate | *isolate-override | *plaintext;

	  [fix]/* 文本效果样式 */
	  [-] font: caption | icon | menu | message-box | small-caption | status-bar | ...;
	    [fix]/* 选择字体风格 */
	    font-style: normal | italic | oblique;
	    [fix]/* 西文字体小写转换大写 */
	    font-variant: normal | none | small-caps...;
	    [fix]/* 指定字重 */
	    font-weight: normal | bold｜lighter | bolder | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900;
	    [fix]/* 对字体进行变形 */
	    font-stretch: normal | ultra-condensed | extra-condensed | condensed | semi-condensed | semi-expanded | expanded | extra-expanded | ultra-expanded;
	    [fix]/* 字体大小 */
	    font-size: <length> | <percentage> | larger | smaller | xx-small | x-small | small | medium | large | x-large | xx-large;
	    [fix]/* 声明渲染字体 */
	    font-family: <family-name> | <generic-name>;
	    [fix]/* 设置行高 */
	    line-height: normal | <number> | <length> | <percentage>;

	  [fix]/* 设置元素前景色 */
	  color: <color>;

	  [fix]/* 设置OpenType字体样式集，https://blogs.msdn.microsoft.com/ie_cn/2012/01/17/css-4 */
	  font-feature-settings: normal | <feature-tag-value>;
		[fix]/* 声明OpenType文本的语言渲染处理 */
		font-language-override: normal | <string>;

	  /*如何处理元素中的空白符*/
	  white-space: normal | pre | nowrap | pre-wrap | pre-line;
	  /*->white-space:nowrap; overflow: hidden;文本溢出处理*/
	  text-overflow: clip | ellipsis | *<string>;

		[fix]/* 字体合成 */
		font-synthesis: none | weight | style;
		[fix]/* 定义字体的aspect值（字体的小写字母x的高度与font-size高度之间的比率被称为一个字体的 aspect 值） */
		font-size-adjust: none | <number>;
	  [fix]/* 定义字间距 */
	  letter-spacing: normal | <length>;

	  [fix]/* 控制西文字符间隙距离 */
	  font-kerning: auto | normal | none;
	  /*声明标签和单词的间距*/
	  word-spacing: normal | <length> | <percentage>;
	  /*控制文本的大小写*/
	  text-transform: none | capitalize | uppercase | lowercase;
	  [fix]/* 是否允许单词中断换行 */
	  overflow-wrap(word-wrap): normal | break-word;
	  /*指定怎样在单词内断行*/
	  word-break: normal | break-all | keep-all;
		[fix]/* 声明文本断行规则 */
		line-break: auto | loose | normal | strict;
	  [fix]/* 西文文本换行时如何处理连字符 */
	  hyphens: none | manual | auto;

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


  [fix]/* 定义图片缩放算法 */
  image-rendering: auto | crisp-edges | pixelated;
  [fix]/* 修正图片的预设方向 */
  image-orientation: from-image | <angle> | flip;
	[fix]/* 设定图片分辨率 */
	image-resolution: <resolution>;

  [fix]/* 替换元素的内容如何适应容器 */
  object-fit: fill | contain | cover | none | scale-down;
  [fix]/* 确定替换元素的位置 */
  object-position: left | center | right | top | bottom | <length> | <percentage>;

  /*当元素之间重叠的时候，决定哪一个元素覆盖在其余元素的上方显示。*/
  z-index: <-integer> | auto;
  /*设置元素的缩放*/
  *zoom: auto | <number> | <percentage>;

  [fix]/* 对元素进行裁剪 */
  clip-path: url | none | <basic-shape> | <geometry-box>;
	[fix]/* 对元素使用遮罩 */
	[-] mask: ...;
		[fix]/* 遮罩层图像 */
		mask-image: none | <url>;
		[fix]/* 遮罩层模式 */
		mask-mode: alpha | luminance | match-source;
		[fix]/* 遮罩层位置 */
		mask-position: <position>;
		[fix]/* 遮罩层大小 */
		mask-size: <length> | <percentage> | auto | cover | contain;
		[fix]/* 遮罩层如何重复性 */
		mask-repeat: repeat-x | repeat-y | repeat | space | round | no-repeat;
		[fix]/* 遮罩层的定位区域 */
		mask-origin: border-box | padding-box | content-box | margin-box | fill-box | stroke-box | view-box;
		[fix]/* 遮罩层的影响范围 */
		mask-clip: border-box | padding-box | content-box | margin-box | fill-box | stroke-box | view-box | no-clip;
		[fix]/* 选择遮罩层的叠加方式 */
		mask-composite: add | subtract | intersect | exclude;
	[fix]/* <mask>标签中遮罩以亮度或是透明度呈现 */
	mask-type: luminance | alpha;



	


	/*是否可由用户调整元素的尺寸*/
	resize: none | both | horizontal | vertical | block | inline;
  [fix]/* 声明鼠标悬浮样式 */
  cursor:  <url> | auto | default | none | context-menu | help | pointer | progress | wait | cell | crosshair | text | vertical-text | alias | copy | move | no-drop | not-allowed | e-resize | n-resize | ne-resize | nw-resize | s-resize | se-resize | sw-resize | w-resize | ew-resize | ns-resize | nesw-resize | nwse-resize | col-resize | row-resize | all-scroll | -zoom-in | -zoom-out | grab | grabbing;

	[fix]/* 声明插入光标的颜色 */
	caret-color: auto | <color>;
	[fix]/* 是否允许激活输入法（IME）状态 */
	ime-mode: auto | normal | active | inactive | disabled;
  /*隐藏元素，并将其所占空间用空白占位*/
  visibility: visible | hidden | collapse;

  [fix]/* 为计数器设置初始值 */
  counter-reset: <custom-ident> <integer> | none;
  [fix]/* 为元素添加计数器 */
  counter-increment: <custom-ident> <integer> | none;
  /* 在::before和::after中插入内容*/
  content: none | normal | <string> | <uri> | <counter> | attr() | open-quote | close-quote | no-open-quote | no-close-quote;

  /*为将要改变的元素提前做优化准备工作*/
  *will-change: auto | scroll-position | contents | <custom-ident>;
  [fix]/* 设置鼠标事件穿透 */
  pointer-events: auto | none | visiblePainted | visibleFill | visibleStroke | visible | painted | fill | stroke | all | inherit;

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

  [fix]/* 设置透视的观测距离 */
  perspective: none | <length>;
  [fix]/* 设置透视的灭点位置 */
  perspective-origin: <x-position> | <y-position> | <percentage> | <length>;

  [fix]/* 3d状态下，声明元素背面是否可见 */
  backface-visibility: visible | hidden;

	[fix]/* 设置元素之前的分页符 */
	page-break-before: auto | always | avoid | left | right;
	[fix]/* 设置元素之后的分页符 */
	page-break-after: auto | always | avoid | left | right;
	[fix]/* 设置元素容器内的分页符 */
	page-break-inside: auto | avoid;

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
  [-] animation: ...;
    [fix]/* 指定应用声明过的动画标识 */
    animation-name: none | <animation-ident>;
    [fix]/* 指定动画执行周期 */
    animation-duration: <time>;
    [fix]/* 定义动画缓动函数 */
    animation-timing-function: <timing-function>;
    [fix]/* 定义延时 */
    animation-delay: <time>;
    [fix]/* 定义动画循环次数 */
    animation-iteration-count: infinite | <number>;
    [fix]/* 指示是否反向播放 */
    animation-direction: normal | reverse | alternate | alternate-reverse;
    [fix]/* 指定动画执行前后的元素样式 */
    animation-fill-mode: none | forwards | backwards | both;
    [fix]/* 定义或查询一个动画的当前状态 */
    animation-play-state: running | paused;
}


```