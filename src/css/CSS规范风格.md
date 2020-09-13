## CSS规范风格

### 概述

CSS作为描述网页形式的核心，其各个属性并不是相互独立的，而是共同作用相辅相成的，且自由度较高。这也容易造成在编写过程中，为了实现预期表现而不断的追加属性施加影响，若不按照属性类型顺序追加，则对于维护者来说就无法第一时间理解原作者的意图，亦或是在达到预期后干扰了其它元素的表现，亦或是没有深入理解属性本身而破坏了原有更加合理的元素结构等等。CSS规范旨在提高可阅读性、保证代码质量、改善协作。



### 命名空间

规划页面布局结构，仅针对业务部分，不限制呈现内容元素通用类型，也不限制通用组件结构类型，如对话框dialog、提示toast等。

|       类型       | 匹配语法 | 描述                                                         | 兄弟关系 | 父子关系 |
| :--------------: | :------: | ------------------------------------------------------------ | :------: | :------: |
|   视图 - view    |    v-    | 页面顶级结构，祖先为容器类名，仅存在一个                     |  不存在  |  不存在  |
|  布局 - layout   |    l-    | 页面次级结构，表示较大范围的页面内容                         |   存在   |  不存在  |
|  模块 - module   |    m-    | 页面模块结构，表示较小范围的页面内容                         |   存在   |  不存在  |
| 组件 - component |    c-    | 组件容器（等同于通用组件类型），表示独立组件级别，范围等同于模块 |   存在   |  不存在  |
|    盒子 - box    |    b-    | 次小级单位容器，表示模块和单元之间的过渡容器，单元容器优先   |   存在   |   存在   |
|   单元  - unit   |    u-    | 最小级单位容器，表示模块和一个以上呈现内容元素之间的容器     |   存在   |  不存在  |



#### 视图示例

```html
<!-- Not recommended -->
<div class="app">
  <div class="header"></div>
  <div class="v-home"></div>
  <div class="v-footer"></div>
</div>

<div class="v-home">
  <div class="v-header"></div>
</div>
```

```html
<!-- Recommended -->
<div class="app">
  <div class="v-home"></div>
</div>
```

通常情况下，针对非单页应用(SPA)，视图层结构可省略。



#### 布局示例

```html
<!-- Not recommended -->
<div class="l-header">
  <div class="l-left"></div>
</div>
```

```html
<!-- Recommended -->
<div class="app">
  <div class="l-header"></div>
  <div class="l-content"></div>
  <div class="dialog"></div>
  <!-- other content -->
</div>
```

通常情况下，若页面层级结构较简单，布局层结构可省略。



#### 模块示例

```html
<!-- Not recommended -->
<div class="m-header">
  <div class="m-left"></div>
</div>
```

```html
<!-- Recommended -->
<div class="app">
  <div class="m-header"></div>
  <div class="l-content"></div>
  <div class="m-footer"></div>
  <div class="dialog"></div>
  <!-- other conetnt -->
</div>
```

通常情况下，模块结构不可省略。



#### 组件示例

参考模块示例



#### 盒子示例

```html
<!-- Not recommended -->
<div class="m-header">
  <div class="b-left">
    <!-- content, more than one children node -->
  </div>
  <div class="b-center">
    <!-- content, more than one children node -->
  </div>
</div>
```

```html
<!-- Recommended -->
<div class="m-header">
  <div class="b-content">
    <div class="u-logo">
      <!-- content, more than one children node -->
    </div>
    <dic class="u-title">
      <!-- content, more than one children node -->
    </dic>
  </div>
</div>

<div class="m-header">
  <div class="b-content">
    <div class="b-left">
      <div class="u-logo">
        <!-- content, more than one children node -->
      </div>
      <!-- content -->
    </div>
    <div class="u-center">
      <!-- content, more than one children node -->
    </div>
  </div>
</div>
```

通常情况下，只有层级结构较深才需要用到盒子容器，且必须有大于一个子节点，单元容器优先级更高。



#### 单元示例

```html
<!-- Not recommended -->
<div class="u-left">
  <div class="u-logo">
    <!-- content, more than one children node -->
  </div>
  <!-- content -->
</div>
```

```html
<!-- Recommended -->
<div class="m-header">
  <div class="u-logo">
    <i class="icon icon-logo"></i>
    <span class="txt-logo"></span>
  </div>
  <!-- conetnt -->
</div>
```

通常情况下，单元容器不可省略，除非多个呈现内容元素无需容器包裹。



### 呈现内容元素通用类型(若和命名空间存在冲突，通用类型优先级更高)

|            类型            | 匹配语法 | 子元素(可选项) | 后代数 |
| :------------------------: | :------: | :------------: | :----: |
|    背景图 - background     |   bg-    |       无       |   0    |
|        图标 - icon         |  icon-   |       无       |   0    |
|       头像 - avatar        | avatar-  |       无       |   0    |
|        图片 - image        |   img-   |       无       |   0    |
|       横幅 - banner        | banner-  |       无       |   0    |
|      通用文本 - text       |   txt-   |       有       |   1    |
|      提示文本 - hint       |  hint-   |       有       |   1    |
| 段落描述文本 - description |  desc-   |       有       |   1    |
|        表单 - input        |  input-  |       无       |   0    |
|       按钮 - button        |   btn-   |       有       |   1    |
|        线条 - line         |  line-   |       无       |   0    |

通常情况下作为实际呈现内容元素展示，特殊情况可以存在子元素。



### 通用组件结构类型(若和命名空间存在冲突，通用类型优先级更高)

若将某个项目内部组件独立成公共组件，则必须以以下类型作为组件顶级元素的类名。

|  类型  | 匹配语法[-] |
| :----: | :---------: |
|  头部  |   header    |
|  内容  |   content   |
|  容器  |  container  |
|  尾部  |   footer    |
| 交互框 |   dialog    |
| 提示框 |    alert    |
|  提示  |    toast    |
| 进度条 |  progress   |
|  标签  |     tab     |
|  菜单  |    menu     |
|  列表  |    list     |
|   项   |    item     |



### [属性书写顺序](https://github.com/jhaofan/jhaofan.github.io/blob/master/src/css/CSS属性描述表.md)



### 不推荐使用方式

| 不推荐等级 | 描述                                   | 原因                                                         |
| :--------: | -------------------------------------- | ------------------------------------------------------------ |
|     3      | 使用!important                         | 严重破坏选择器匹配权重关系，给协作和维护带来噩梦般的影响，除极其特殊的情况 |
|     2      | 初始化元素属性 box-sizing: border-box; | 破坏元素盒结构且非必要性                                     |
|     2      | 使用通用选择器 *                       | 性能较差，可用场景较少，如富文本元素初始化                   |
|     1      | 类结构嵌套三级以上                     | 可维护性差，必然可优化                                       |
|     1      | 使用ID选择器                           | 一定程度破坏选择器匹配权重关系，必然可优化                   |



### [编写规范参考Google Style Guides CSS部分](https://google.github.io/styleguide/htmlcssguide.html#CSS)



### [注释规范参考KSS](http://warpspire.com/kss/syntax/)

