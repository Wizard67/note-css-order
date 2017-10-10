```css
/* 表示距离尺寸 */
<length>: .em | .ex | .ch | .rem | .lh | .rlh | .vh | .vw | .vi | .vb | .wmin | .vmax | .px | .mm | .cm | .in | .pt | .pc | .mozmm;
/* 表示一个百分百值 */
<percentages>: .%;
/* 指向一个资源 */
<url>: url();
/* 表示数字 */
<number>: 0 | 0.0 | -0 | +0;
/* 表示颜色 */
<color>: <hex-color> | <named-color> | transparent | currentcolor | <rgb()> | <hsl()> | <rgba()> | <hsla()> | <deprecated-system-color>;
/* 表示形状 */
<shape>: rect(<top>, <right>, <bottom>, <left>);
/* 表示时间 */
<time>: .ms | .s;


div {
  /* 设置元素的定位方式 */
  position: static | relative | absolute | fixed | sticky;
  /* 使定位后的元素产生位置偏移 */
  top: <length> | <percentages> | auto;
  right: <length> | <percentages> | auto;
  bottom: <length> | <percentages> | auto;
  left: <length> | <percentages> | auto;

	/* 元素浮动 */
	float: left | right | none | inline-start | inline-end;
	/* 是否清除浮动 */
	clear: none | left | right | both | inline-start | inline-end;

  /* 描述元素的盒子类型 */
  display: none | inline | block | list-item | inline-list-item | inline-block | inline-table | table | table-cell | table-column | table-column-group | table-footer-group | table-header-group | table-row | table-row-group | flex | inline-flex | grid | inline-grid | run-in | ruby | ruby-base | ruby-text | ruby-base-container | ruby-text-container | contents;

	/* 声明项目的空间分配 */
	[-] flex: auto | initial | none | ...;
	  /* 定义项目的拉伸因子 */
	  flex-grow: <number>;
	  /* 定义项目的收缩规则 */
	  flex-shrink: <number>;
	  /* 指定项目在主轴方向的初始大小 */
	  flex-basis: <length> | <percentages> | content;
	/* 声明容器的主轴方向和换行规则 */
	[-] flex-flow: ...;
		/* 定义主轴的方向 */
		flex-direction: row | row-reverse | column | column-reverse;
		/* 声明是否允许换行 */
		flex-wrap: nowrap | wrap | wrap-reverse;
	/* 声明项目在主轴上的位置和空间分配 */
	justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
	/* 声明如何分配多行弹性容器中侧轴的空间位置 */
	align-content: flex-start | flex-end | center | space-between | space-around | stretch;
	/* 声明项目在侧轴上的位置和空间分配 */
	align-items: flex-start | flex-end | center | baseline | stretch;
	/* 单独声明项目在弹性容器侧轴上的对齐方式 */
	align-self: auto | flex-start | flex-end | center | baseline | stretch;
	/* 项目在弹性容器中的排序权重 */
	order: <integer>;


	/* 声明网格容器属性 */
	[-] grid: ...;
		/* 声明横向网格线名称和网格高度 */
		grid-template-rows: none | auto | [linename] | <length> | <percentage> | <flex> | max-content | min-content | minmax() | fit-content() | repeat();
		/* 声明纵向网格线名称和网格宽度 */
		grid-template-columns: none | auto | [linename] | <length> | <percentage> | <flex> | max-content | min-content | minmax() | fit-content() | repeat();
		/* 声明网格区域名称 */
		grid-template-areas: none | <string> | .;
		/* 声明隐式网格行*/
		grid-auto-rows: auto | <length> | <percentage> | <flex> | max-content | min-content | minmax();
		/* 声明隐式网格列*/
		grid-auto-columns:  auto | <length> | <percentage> | <flex> | max-content | min-content | minmax() | fit-content();
		/* 定义网格流方向 */
		grid-auto-flow: row | column | dense;
		/* 设置网格列之间的间距 */
		grid-column-gap: <length> | <percentage>;
		/* 设置网格行之间的间距 */
		grid-row-gap: <length> | <percentage>;

	/* 声明网格项目位置的合并 */
	[-] grid-area: <custom-ident> | ...;
		/* 声明网格项目行合并的初始位置 */
		grid-row-start: auto | span | <integer> | <custom-ident>;
		/* 声明网格项目行合并的结束位置 */
		grid-row-end: auto | span | <integer> | <custom-ident>;
		/* 声明网格项目行合并的初始位置 */
		grid-column-start: auto | span | <integer> | <custom-ident>;
		/* 声明网格项目列合并的结束位置 */
		grid-column-end: auto | span | <integer> | <custom-ident>;

	/* 声明网格项目行的合并 */
	[-] grid-column: ...;
		grid-column-start: ;
		grid-column-end: ;

	/* 声明网格行列间距 */
	[-] grid-gap: ...;
		grid-row-gap: ;
		grid-column-gap: ;

	/* 声明网格项目列的合并 */
	[-] grid-row: ...;
		grid-row-start: ;
		grid-row-end: ;

	/* 声明网格容器属性 */
	[-] grid-template: ...;
		grid-template-rows: ;
		grid-template-columns: ;
		grid-template-areas: ;
	
	/* 定义了表格布局算法 */
	table-layout: auto | fixed;
	/* 表格空单元格的样式显示处理 */
	empty-cells: show | hide;
	/* 规定表格标题放置位置 */
	caption-side: top | bottom | block-start | block-end | inline-start | inline-end;
	/* 声明表格的边框是分隔还是合并 */
	border-collapse: collapse | separate;
	/* 设置相邻单元格边框之间的边距 */
	border-spacing: <length> ;

	/* 设置列表符号 */
 	[-] list-style: ...;
	  /* 列表符号风格 */
	  list-style-type: none | <counter-style> | <string>;
	  /* 列表符号定位 */
	  list-style-position: inside | outside;
	  /* 指定图片作为列表符号 */
	  list-style-image: none | <url>;


  /* 改变默认的CSS盒模型对元素宽高的计算方式 */
  box-sizing: content-box | border-box;
	/* 指定了元素内容区的宽度。*/
	width: <length> | <percentage> | auto | max-content | min-content | fill-available | fit-content;
	 /* 为元素设置最小宽度 */
	min-width: <length> | <percentage> | max-content | min-content | fill-available | fit-content;
	/* 为元素内容区设置最大宽度值 */
	max-width: none | <length> | <percentage> | max-content | min-content | fill-available | fit-content;

	/* 指定了元素内容区的高度 */
	height: <length> | <percentage> | auto;
	/* 为元素设置最小高度 */
	min-height: <length> | <percentage> | max-content | min-content | fill-available | fit-content;
	/* 为元素内容区设置最大高度值 */
	max-height: none | <length> | <percentage> | max-content | min-content | fill-available | fit-content;

	/* 为元素声明内边距 */
	[-] padding: <length> | <percentage>;
	  padding-top: ;
	  padding-right: ;
	  padding-bottom: ;
	  padding-left: ;

	/* 声明边框属性 */
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
	      border-image-source: none | <url>;
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

	/* 为元素设置轮廓线 */
	[-] outline: ...;
	  /* 设置轮廓线宽度 */
	  outline-width: <length> | thin | medium | thick;
	  /* 为轮廓线设置颜色 */
	  outline-color: <color> | inver;
	  /* 轮廓线风格 */
	  outline-style: auto | none | dotted | dashed | solid | double | groove | ridge | inset | outset;
	/* 对轮廓进行偏移 */
	outline-offset: <length>;

	/* 为元素声明外边距 */
	[-] margin: <length> | <percentage> | auto;
	  margin-top: ;
	  margin-right: ;
	  margin-bottom: ;
	  margin-left: ;

	/* 声明背景属性 */
	[-] background: ...;
	  /* 为元素设置一个或多个背景图像 */
	  background-image: none | <url>;
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

	/* 背景图片以及背景色的混合模式 */
	background-blend-mode: <blend-mode>;
	/* 定义元素是否创建新的混合环境 */
	isolation: auto | isolate;

	/* 设置元素投影 */
	box-shadow: inset | <offset-x> <offset-y> | <blur-radius> | <spread-radius> | <color>;

	 /* 设置透明度 */
	opacity: <number>;
	/* 滤镜属性 */
	filter: <url> | <filter-function>;


  /* 设置列属性 */
  [-] columns: ...;
    /* 设置列的宽度 */
    column-width: <length> | auto;
    /* 设置被划分的列数 */
    column-count: <number> | auto;
  /* 声明列之间的间隔 */
  column-gap: <length> | normal;
  /* 声明列的样式 */
  [-] column-rule: ...;
    /* 列之间的宽度 */
    column-rule-width: <length> | thin | medium | thick;
    /* 列之间的分割样式 */
    column-rule-style: none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset;
    /* 列之间的颜色 */
    column-rule-color: <color>;
  /* 规定元素横跨列数 */
  column-span: none | all;
  /* 指定留在容器底部元素最小行的数量 */
  orphans: <integer>;
	/* 声明内容如何分割成列 */
	column-fill: auto | balance;


  /* 规定了内容溢出容器时的处理 */
  overflow: ...;
    /* 水平溢出的处理 */
    overflow-x: visible | hidden | scroll | auto;
    /* 垂直溢出的处理 */
    overflow-y: visible | hidden | scroll | auto;


  /* 指定行内元素或表格单元格元素的垂直对齐方式 */
  vertical-align: baseline | sub | super | text-top | text-bottom | middle | top | bottom | <percentage> | <length>;

  /* 定义如何渲染字体 */
  text-rendering: auto | optimizeSpeed | optimizeLegibility | geometricPrecision;

	  /* 规定文本的排版模式 */
	  writing-mode: horizontal-tb | vertical-rl | vertical-lr | sideways-rl | sideways-lr;
	  /* 纵横混排 */
	  text-combine-upright: none | all | <integer>;
	  /* 控制字符方向 */
	  text-orientation: mixed | upright | sideways;
	  /* 规定文本书写方向 */
	  direction: ltr | rtl;
	  /* 双向排列 */
	  unicode-bidi: normal | embed | bidi-override | isolate | isolate-override | plaintext;

	  /* 文本效果样式 */
	  [-] font: caption | icon | menu | message-box | small-caption | status-bar | ...;
	    /* 选择字体风格 */
	    font-style: normal | italic | oblique;
	    /* 西文字体小写转换大写 */
	    font-variant: normal | none | small-caps...;
	    /* 指定字重 */
	    font-weight: normal | bold｜lighter | bolder | 100 | 200 | 300 | 400 | 500 | 600 | 700 | 800 | 900;
	    /* 对字体进行变形 */
	    font-stretch: normal | ultra-condensed | extra-condensed | condensed | semi-condensed | semi-expanded | expanded | extra-expanded | ultra-expanded;
	    /* 字体大小 */
	    font-size: <length> | <percentage> | larger | smaller | xx-small | x-small | small | medium | large | x-large | xx-large;
	    /* 声明渲染字体 */
	    font-family: <family-name> | <generic-name>;
	    /* 设置行高 */
	    line-height: normal | <number> | <length> | <percentage>;

	  /* 设置元素前景色 */
	  color: <color>;

	  /* 设置OpenType字体样式集，https://blogs.msdn.microsoft.com/ie_cn/2012/01/17/css-4 */
	  font-feature-settings: normal | <feature-tag-value>;
		/* 声明OpenType文本的语言渲染处理 */
		font-language-override: normal | <string>;

	  /* 处理元素中的空白符 */
	  white-space: normal | pre | nowrap | pre-wrap | pre-line;
	  /* 文本溢出处理 white-space:nowrap; overflow: hidden;*/
	  text-overflow: clip | ellipsis | <string>;

		/* 字体合成 */
		font-synthesis: none | weight | style;
		/* 定义字体的aspect值（字体的小写字母x的高度与font-size高度之间的比率被称为一个字体的 aspect 值） */
		font-size-adjust: none | <number>;
	  /* 定义字间距 */
	  letter-spacing: normal | <length>;

	  /* 控制西文字符间隙距离 */
	  font-kerning: auto | normal | none;
	  /* 声明标签和单词的间距 */
	  word-spacing: normal | <length> | <percentage>;
	  /* 控制文本大小写 */
	  text-transform: none | capitalize | uppercase | lowercase | full-width;
	  /* 是否允许单词中断换行 */
	  overflow-wrap(word-wrap): normal | break-word;
	  /* 声明单词断行规则 */
	  word-break: normal | break-all | keep-all;
		/* 声明文本断行规则 */
		line-break: auto | loose | normal | strict;
	  /* 西文文本换行时如何处理连字符 */
	  hyphens: none | manual | auto;

	  /* 定义元素内的内容如何对齐  */
	  text-align: start | end | left | right | center | justify | match-parent;
	  /* 规定如何对齐末行元素 */
	  text-align-last: auto | start | end | left | right | center | justify;
		/* 文本两侧对齐时的空白填充方式 */
		text-justify: auto | inter-character | inter-word | none;

	  /* 为元素内容添加引用符号 */
	  quotes: none | <string>;
	  /* 制表符（U+0009）宽度 */
	  tab-size: <integer> | <length>;
	  /* 文本首行缩进 */
	  text-indent: <length> | <percentage> | hanging | each-line;
	  /* 文本重点标记 */
	  [-] text-emphasis: ...;
			/* 标记符号的类型 */
			text-emphasis-style: none | open | dot | circle | double-circle | triangle | sesame | <string>;
			/* 标记符号的颜色 */
	    text-emphasis-color: <color>;
		  /* 文本重点标记的渲染位置 */
	    text-emphasis-position: over | under | right | left;
	    
	  /* 文本修饰线 */
	  [-] text-decoration: ...;
			/* 文本修饰线的颜色 */
	    text-decoration-color: <color>;
			/* 文本修饰线的类型 */
	    text-decoration-style: solid | double | dotted | dashed | wavy;
			/* 文本修饰线的渲染位置 */
	    text-decoration-line: none | underline | overline | line-through | blink;
	  /* 文本下划线位置 */
	  text-underline-position: auto | under | left | right | under left | right under;

	  /* 文本阴影 */
	  text-shadow: none | <color> | <offset-x> <offset-y> | <blur-radius>;


	/* 设定alpha值提取图像形状 */
	shape-image-threshold: <number>;
	/* 为形状（shape）添加轮廓 */
	shape-outside: none | <shape-box> | <basic-shape> | <url>;
	/* 为形状（shape）添加外边距 */
	shape-margin: <length> | <percentage>;


  /* 定义图片缩放算法 */
  image-rendering: auto | crisp-edges | pixelated;
  /* 修正图片的预设方向 */
  image-orientation: from-image | <angle> | flip;
	/* 设定图片分辨率 */
	image-resolution: <resolution>;

  /* 替换元素的内容如何适应容器 */
  object-fit: fill | contain | cover | none | scale-down;
  /* 确定替换元素的位置 */
  object-position: left | center | right | top | bottom | <length> | <percentage>;

  /* 声明元素重叠时显示的权重 */
  z-index: <integer> | auto;

	/* 自定义属性 */
	--*: ...;

  /* 对元素进行裁剪 */
  clip-path: url | none | <basic-shape> | <geometry-box>;
	/* 对元素使用遮罩 */
	[-] mask: ...;
		/* 遮罩层图像 */
		mask-image: none | <url>;
		/* 遮罩层模式 */
		mask-mode: alpha | luminance | match-source;
		/* 遮罩层位置 */
		mask-position: <position>;
		/* 遮罩层大小 */
		mask-size: <length> | <percentage> | auto | cover | contain;
		/* 遮罩层如何重复性 */
		mask-repeat: repeat-x | repeat-y | repeat | space | round | no-repeat;
		/* 遮罩层的定位区域 */
		mask-origin: border-box | padding-box | content-box | margin-box | fill-box | stroke-box | view-box;
		/* 遮罩层的影响范围 */
		mask-clip: border-box | padding-box | content-box | margin-box | fill-box | stroke-box | view-box | no-clip;
		/* 选择遮罩层的叠加方式 */
		mask-composite: add | subtract | intersect | exclude;
	/* <mask>标签中遮罩以亮度或是透明度呈现 */
	mask-type: luminance | alpha;

	/* 注释的对齐方式 */
	ruby-align: start | center | space-between | space-around;
	/* 在一个ruby容器内如何处理多个注释 */
	ruby-merge: auto | collapse | separate;
	/* 注释的放置位置 */
	ruby-position: over | under | inter-character;
	


	/* 是否可由用户调整元素的尺寸 */
	resize: none | both | horizontal | vertical;
  /* 声明鼠标悬浮样式 */
  cursor:  <url> | auto | default | none | context-menu | help | pointer | progress | wait | cell | crosshair | text | vertical-text | alias | copy | move | no-drop | not-allowed | e-resize | n-resize | ne-resize | nw-resize | s-resize | se-resize | sw-resize | w-resize | ew-resize | ns-resize | nesw-resize | nwse-resize | col-resize | row-resize | all-scroll | -zoom-in | -zoom-out | grab | grabbing;

	/* 声明插入光标的颜色 */
	caret-color: auto | <color>;
	/* 是否允许激活输入法（IME）状态 */
	ime-mode: auto | normal | active | inactive | disabled;
	/* 隐藏元素保留空间位置 */
  visibility: visible | hidden | collapse;

	/* 规定用户手势操作方式 */
	touch-action: auto | none | pan-x | pan-left | pan-right | pan-y | pan-up | pan-down | pinch-zoom | manipulation;
  /* 为计数器设置初始值 */
  counter-reset: <custom-ident> <integer> | none;
  /* 为元素添加计数器 */
  counter-increment: <custom-ident> <integer> | none;
  /* 在::before和::after中插入内容*/
  content: none | normal | <string> | <uri> | <counter> | attr() | open-quote | close-quote | no-open-quote | no-close-quote;

   /* 通知浏览器进行元素改变的优化 */
  will-change: auto | scroll-position | contents | <custom-ident>;
  /* 设置鼠标事件穿透 */
  pointer-events: auto | none | visiblePainted | visibleFill | visibleStroke | visible | painted | fill | stroke | all | inherit;

   /* 重置除了 unicode-bidi 和 direction 之外的所有属性至初始值或继承值 */
  all: initial | inherit | unset;

  /* 子元素空间状态（2d/3d）*/
  transform-style: flat | preserve-3d;
  /* 元素变形 */
  transform: none | <transform-function>;
  /* 元素变形范围 */
  transform-box: border-box | fill-box | view-box;
  /* 元素变形的中心点*/
  transform-origin: <percentage> | <length> | left | center | right | top | bottom | center;

  /* 设置透视的观测距离 */
  perspective: none | <length>;
  /* 设置透视的灭点位置 */
  perspective-origin: <x-position> | <y-position> | <percentage> | <length>;

  /* 3d状态下，声明元素背面是否可见 */
  backface-visibility: visible | hidden;

	/* 设置元素之前的分页符 */
	page-break-before: auto | always | avoid | left | right;
	/* 设置元素之后的分页符 */
	page-break-after: auto | always | avoid | left | right;
	/* 设置元素容器内的分页符 */
	page-break-inside: auto | avoid;
	/* 页面打印时分页保留的最少行数 */
	widows: <integer>;

	/* 导航或者CSSOM api产生滚动的过渡效果 */
	scroll-behavior: auto | smooth;
	/* 定义元素滚动的snap点类型 */
	scroll-snap-type: none | mandatory | proximity;
	/* 定义元素滚动的snap点坐标位置*/
	scroll-snap-destination: <position>;
	/* 定义元素滚动的snap点坐标偏移位置 */
	scroll-snap-coordinate: none | <position>;


  /* 定义元素过渡效果 */
  [-] transition: none | ...;
	  /* 指定需过渡的属性 */
    transition-property: none | all | <transition-ident>;
    /* 过渡效果执行时间 */
    transition-duration: <time>;
    /* 定义过渡缓动函数 */
    transition-timing-function: <timing-function>;
    /* 延迟过渡 */
    transition-delay: <time>;


  /* 动画属性 */
  [-] animation: ...;
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