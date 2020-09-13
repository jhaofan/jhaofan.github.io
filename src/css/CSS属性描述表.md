## CSS属性描述表

### 概述

属性描述表主要收录了常用属性，并突出属性特点，制定类型顺序约束编写规范，提供对应属性草案链接。



### 类型顺序

以显示元素及其内容作为基础标准，定义类型编写先后顺序。

- position - 定位

- content - 内容

- visibility - 可见性

- box - 盒模型

- font - 文本

- background - 背景

- border - 边框

- outline - 外边框

- border-radius - 边框圆角

- transform - 变化

- animation - 动画

- transition - 过渡效果

- other - 其它



### 简写规则

属性往往由多个单词通过**-**符号组合而成，默认简写取各个单词首字母，如`display = d`、`font-size = fs`。若遇到简写冲突，按照类型顺序修改优先级较低的属性，取单词重音字母进行组合或一整个短单词，如若padding比position优先级较低，则`padding = pd`。若属性名是某个属性名的衍生，则延用，如若`background = bg`，则`background-color = bgc`。



### 属性描述表

|   类型顺序    |                             属性                             | 简写  |         初始值          |
| :-----------: | :----------------------------------------------------------: | :---: | :---------------------: |
|   position    | [position](https://www.w3.org/TR/2016/WD-css-position-3-20160517/#position-property) |  @p   |         static          |
|               | [top](https://www.w3.org/TR/2016/WD-css-position-3-20160517/#box-offsets-trbl) |  @t   |          auto           |
|               | [bottom](https://www.w3.org/TR/2016/WD-css-position-3-20160517/#box-offsets-trbl) |  @b   |          auto           |
|               | [left](https://www.w3.org/TR/2016/WD-css-position-3-20160517/#box-offsets-trbl) |  @l   |          auto           |
|               | [right](https://www.w3.org/TR/2016/WD-css-position-3-20160517/#box-offsets-trbl) |  @r   |          auto           |
|               | [z-index](https://www.w3.org/TR/2016/WD-css-position-3-20160517/#layered-presentation) |  @zi  |          auto           |
|    content    | [content](https://www.w3.org/TR/css-content-3/#property-index) |  @c   |         normal          |
|  visibility   | [overflow](https://www.w3.org/TR/css-overflow-3/#overflow-properties) |  @o   |     visible visible     |
|               | [overflow-y](https://www.w3.org/TR/css-overflow-3/#overflow-properties) |  @oy  |         visible         |
|               | [overflow-x](https://www.w3.org/TR/css-overflow-3/#overflow-properties) |  @ox  |         visible         |
|               |    [opacity](https://www.w3.org/TR/css-color-3/#opacity)     |  @op  |            1            |
|      box      | [order](https://www.w3.org/TR/css-flexbox-1/#order-property) |  @od  |            0            |
|               |  [flex](https://www.w3.org/TR/css-flexbox-1/#flex-property)  |  @f   |        0 1 auto         |
|               | [flex-grow](https://www.w3.org/TR/css-flexbox-1/#flex-grow-property) |  @fg  |            0            |
|               | [flex-shrink](https://www.w3.org/TR/css-flexbox-1/#flex-shrink-property) |  @fs  |            1            |
|               | [flex-basis](https://www.w3.org/TR/css-flexbox-1/#flex-basis-property) |  @fb  |          auto           |
|               | [align-self](https://www.w3.org/TR/css-flexbox-1/#align-items-property) |  @as  |         stretch         |
|               | [float](https://www.w3.org/TR/CSS22/visuren.html#propdef-float) |  @fl  |          none           |
|               | [clear](https://www.w3.org/TR/CSS22/visuren.html#propdef-clear) |  @cl  |          none           |
|               | [display](https://www.w3.org/TR/css-display-3/#propdef-display) |  @d   |         inline          |
|               | [flex-flow](https://www.w3.org/TR/css-flexbox-1/#flex-flow-property) |  @ff  |       row nowrap        |
|               | [flex-direction](https://www.w3.org/TR/css-flexbox-1/#flex-direction-property) |  @fd  |           row           |
|               | [flex-wrap](https://www.w3.org/TR/css-flexbox-1/#flex-wrap-property) |  @fw  |         nowrap          |
|               | [justify-content](https://www.w3.org/TR/css-flexbox-1/#justify-content-property) |  @jc  |       flex-start        |
|               | [align-items](https://www.w3.org/TR/css-flexbox-1/#align-items-property) |  @ai  |         stretch         |
|               | [align-content](https://www.w3.org/TR/css-flexbox-1/#align-content-property) |  @ac  |         stretch         |
|               | [box-sizing](https://www.w3.org/TR/css-sizing-3/#propdef-box-sizing) |  @bs  |       content-box       |
|               | [width](https://www.w3.org/TR/css-sizing-3/#preferred-size-properties) |  @w   |          auto           |
|               | [height](https://www.w3.org/TR/css-sizing-3/#preferred-size-properties) |  @h   |          auto           |
|               | [min-width](https://www.w3.org/TR/css-sizing-3/#min-size-properties) |  @mw  |          auto           |
|               | [min-height](https://www.w3.org/TR/css-sizing-3/#min-size-properties) |  @mh  |          auto           |
|               | [max-width](https://www.w3.org/TR/css-sizing-3/#max-size-properties) | @maxw |          none           |
|               | [max-height](https://www.w3.org/TR/css-sizing-3/#max-size-properties) | @maxh |          none           |
|               | [margin](https://www.w3.org/TR/css-box-3/#margin-shorthand)  |  @m   |            0            |
|               | [margin-top](https://www.w3.org/TR/css-box-3/#margin-physical) |  @mt  |            0            |
|               | [margin-bottom](https://www.w3.org/TR/css-box-3/#margin-physical) |  @mb  |            0            |
|               | [margin-left](https://www.w3.org/TR/css-box-3/#margin-physical) |  @ml  |            0            |
|               | [margin-right](https://www.w3.org/TR/css-box-3/#margin-physical) |  @mr  |            0            |
|               | [padding](https://www.w3.org/TR/css-box-3/#padding-shorthand) |  @pd  |            0            |
|               | [padding-top](https://www.w3.org/TR/css-box-3/#padding-physical) | @pdt  |            0            |
|               | [padding-bottom](https://www.w3.org/TR/css-box-3/#padding-physical) | @pdb  |            0            |
|               | [padding-left](https://www.w3.org/TR/css-box-3/#padding-physical) | @pdl  |            0            |
|               | [padding-right](https://www.w3.org/TR/css-box-3/#padding-physical) | @pdr  |            0            |
|     font      |     [font](https://www.w3.org/TR/css-fonts-4/#font-prop)     |  @ft  |     对应属性初始值      |
|               | [font-family](https://www.w3.org/TR/css-fonts-4/#font-family-prop) | @ftf  |      取决于浏览器       |
|               | [font-size](https://www.w3.org/TR/css-fonts-4/#font-size-prop) | @fts  |         medium          |
|               | [font-weight](https://www.w3.org/TR/css-fonts-4/#font-weight-prop) | @ftw  |         normal          |
|               | [font-style](https://www.w3.org/TR/css-fonts-4/#font-style-prop) | @ftst |         normal          |
|               | [text-decoration](https://www.w3.org/TR/css-text-decor-3/#text-decoration-property) |  @td  | none solid currentcolor |
|               | [text-decoration-line](https://www.w3.org/TR/css-text-decor-3/#text-decoration-line-property) | @tdl  |          none           |
|               | [text-decoration-style](https://www.w3.org/TR/css-text-decor-3/#text-decoration-style-property) | @tds  |          solid          |
|               | [text-decoration-color](https://www.w3.org/TR/css-text-decor-3/#text-decoration-color-property) | @tdc  |      currentcolor       |
|               |  [color](https://www.w3.org/TR/css-color-4/#propdef-color)   |  @cl  |          black          |
|               | [direction](https://www.w3.org/TR/css-writing-modes-3/#propdef-direction) |  @dr  |           ltr           |
|               | [text-align](https://www.w3.org/TR/css-text-3/#text-align-property) |  @ta  |          start          |
|               | [letter-spacing](https://www.w3.org/TR/css-text-3/#propdef-letter-spacing) |  @ls  |         normal          |
|               | [line-height](https://www.w3.org/TR/CSS22/visudet.html#propdef-line-height) |  @lh  |         normal          |
|               | [vertical-align](https://www.w3.org/TR/CSS22/visudet.html#propdef-vertical-align) |  @va  |        baseline         |
|               | [word-break](https://www.w3.org/TR/css-text-3/#word-break-property) |  @wb  |         normal          |
|               | [word-wrap](https://www.w3.org/TR/css-text-3/#overflow-wrap-property) |  @ww  |         normal          |
|               | [white-space](https://www.w3.org/TR/css-text-3/#propdef-white-space) |  @ws  |         normal          |
|               | [text-overflow](https://drafts.csswg.org/css-ui-3/#text-overflow) |  @to  |          clip           |
|  background   | [background](https://www.w3.org/TR/css-backgrounds-3/#the-background) |  @bg  |     对应属性初始值      |
|               | [background-color](https://www.w3.org/TR/css-backgrounds-3/#the-background-color) | @bgc  |       transparent       |
|               | [background-image](https://www.w3.org/TR/css-backgrounds-3/#the-background-image) | @bgi  |          none           |
|               | [background-size](https://www.w3.org/TR/css-backgrounds-3/#the-background-size) | @bgs  |          auto           |
|               | [background-position](https://www.w3.org/TR/css-backgrounds-3/#the-background-position) | @bgp  |          0% 0%          |
|               | [background-repeat](https://www.w3.org/TR/css-backgrounds-3/#the-background-repeat) | @bgr  |         repeat          |
|    border     | [border](https://www.w3.org/TR/css-backgrounds-3/#the-border-shorthands) |  @bd  |     对应属性初始值      |
|               | [border-style](https://www.w3.org/TR/css-backgrounds-3/#the-border-style) | @bds  |          none           |
|               | [border-width](https://www.w3.org/TR/css-backgrounds-3/#the-border-width) | @bdw  |         medium          |
|               | [border-color](https://www.w3.org/TR/css-backgrounds-3/#the-border-color) | @bdc  |      currentColor       |
|               | [border-top](https://www.w3.org/TR/css-backgrounds-3/#the-border-shorthands) | @bdt  |     对应属性初始值      |
|               | [border-top-style](https://www.w3.org/TR/css-backgrounds-3/#the-border-style) | @bdts |          none           |
|               | [border-top-width](https://www.w3.org/TR/css-backgrounds-3/#the-border-width) | @bdtw |         medium          |
|               | [border-top-color](https://www.w3.org/TR/css-backgrounds-3/#the-border-color) | @bdtc |      currentColor       |
|               | [border-bottom](https://www.w3.org/TR/css-backgrounds-3/#the-border-shorthands) | @bdb  |     对应属性初始值      |
|               | [border-bottom-style](https://www.w3.org/TR/css-backgrounds-3/#the-border-style) | @bdbs |          none           |
|               | [border-bottom-width](https://www.w3.org/TR/css-backgrounds-3/#the-border-width) | @bdbw |         medium          |
|               | [border-bottom-color](https://www.w3.org/TR/css-backgrounds-3/#the-border-color) | @bdbc |      currentColor       |
|               | [border-left](https://www.w3.org/TR/css-backgrounds-3/#the-border-shorthands) | @bdl  |     对应属性初始值      |
|               | [border-left-style](https://www.w3.org/TR/css-backgrounds-3/#the-border-style) | @bdls |          none           |
|               | [border-left-width](https://www.w3.org/TR/css-backgrounds-3/#the-border-width) | @bdlw |         medium          |
|               | [border-left-color](https://www.w3.org/TR/css-backgrounds-3/#the-border-color) | @bdlc |      currentColor       |
|               | [border-right](https://www.w3.org/TR/css-backgrounds-3/#the-border-shorthands) | @bdr  |     对应属性初始值      |
|               | [border-right-style](https://www.w3.org/TR/css-backgrounds-3/#the-border-style) | @bdrs |          none           |
|               | [border-right-width](https://www.w3.org/TR/css-backgrounds-3/#the-border-width) | @bdrw |         medium          |
|               | [border-right-color](https://www.w3.org/TR/css-backgrounds-3/#the-border-color) | @bdrc |      currentColor       |
|    outline    |      [outline](https://www.w3.org/TR/css-ui-3/#outline)      |  @ol  |     对应属性初始值      |
|               | [outline-style](https://www.w3.org/TR/css-ui-3/#outline-style) | @ols  |          none           |
|               | [outline-width](https://www.w3.org/TR/css-ui-3/#outline-width) | @olw  |         medium          |
|               | [outline-color](https://www.w3.org/TR/css-ui-3/#outline-color) | @olc  |         invert          |
|               | [outline-offset](https://www.w3.org/TR/css-ui-3/#outline-offset) | @olo  |            0            |
| border-radius | [border-radius](https://www.w3.org/TR/css-backgrounds-3/#the-border-radius) |  @br  |         0 0 0 0         |
|               | [border-top-left-radius](https://www.w3.org/TR/css-backgrounds-3/#the-border-radius) | @btlr |            0            |
|               | [border-top-right-radius](https://www.w3.org/TR/css-backgrounds-3/#the-border-radius) | @btrr |            0            |
|               | [border-bottom-left-radius](https://www.w3.org/TR/css-backgrounds-3/#the-border-radius) | @bblr |            0            |
|               | [border-bottom-right-radius](https://www.w3.org/TR/css-backgrounds-3/#the-border-radius) | @bbrr |            0            |
|   transform   | [transform](https://drafts.csswg.org/css-transforms/#transform-property) |  @tf  |          none           |
|   animation   | [animation](https://www.w3.org/TR/css-animations-1/#animation) |  @a   |     对应属性初始值      |
|               | [animation-name](https://www.w3.org/TR/css-animations-1/#animation-name) |  @an  |          none           |
|               | [animation-duration](https://www.w3.org/TR/css-animations-1/#animation-duration) |  @ad  |           0s            |
|               | [animation-timing-function](https://www.w3.org/TR/css-animations-1/#animation-timing-function) | @atf  |          ease           |
|               | [animation-iteration-count](https://www.w3.org/TR/css-animations-1/#animation-iteration-count) | @aic  |            1            |
|               | [animation-direction](https://www.w3.org/TR/css-animations-1/#animation-direction) |  @ad  |         normal          |
|               | [animation-play-state](https://www.w3.org/TR/css-animations-1/#animation-play-state) | @aps  |         running         |
|               | [animation-delay](https://www.w3.org/TR/css-animations-1/#animation-delay) | @adl  |           0s            |
|               | [animation-fill-mode](https://www.w3.org/TR/css-animations-1/#animation-fill-mode) | @afm  |          none           |
|  transition   | [transition](https://www.w3.org/TR/css-transitions-1/#transition-shorthand-property) |  @ts  |     对应属性初始值      |
|               | [transition-property](https://www.w3.org/TR/css-transitions-1/#transition-property-property) | @tsp  |           all           |
|               | [transition-duration](https://www.w3.org/TR/css-transitions-1/#transition-duration-property) | @tsd  |           0s            |
|               | [transition-timing-function](https://www.w3.org/TR/css-transitions-1/#transition-timing-function-property) | @tstf |          ease           |
|               | [transition-delay](https://www.w3.org/TR/css-transitions-1/#transition-delay-property) | @tsd  |           0s            |
|     other     | [pointer-events](https://www.w3.org/TR/SVG/interact.html#PointerEventsProp) |  @pe  |     visiblePainted      |

