##Header
固定在头部，可以包含标题标签，可以有左右按钮  样式:bar bar-header  bar-light  
第一个小节  第二个表示的是头部  第三个表示颜色
>子头部，需要在ion-content加入bar-subheader  在头部加上has-subheader不然顶部会被遮挡。

```javascript
    <div class="bar bar-header bar-light">
        <h1 class="title">bar-light</h1>
    </div>
```
##Content
为主题部分，可以自动超出滚动。  
>pull-to-refresh 拉动刷新  ionrefresher
>不断刷新   ionInfiniteScroll

```java
<div class="bar bar-footer bar-balanced">
  <div class="title">Footer</div>
</div>
```

##Footer
在屏幕的底部，可以包含很多元素。内部的title默认居中。
前后按钮一个左，一个右。分别在title两侧。
如果没有title可使用pull-right按钮右对齐。
```java
<div class="bar bar-footer">
  <button class="button button-clear">Left</button>
  <div class="title">Title</div>
  <button class="button button-clear">Right</button>
</div>
////////////////////////////////////////////////
<div class="bar bar-footer">
  <button class="button button-clear pull-right">Right</button>
</div>
```
##Buttons
当按钮应用做Header或者Footer的时候，默认样式为bar，所以需要用额外的样式
，添加希望加上的。
>默认为dispay:inline-block；  
>button-block有Padding。  
>button-full是全屏的，它父级是没有padding的；  
>按钮是有不同尺寸的 button-small    button-large
>button-clear它会移除边框，使得文字脱颖而出。文字的颜色会替换背景色  
>button-outline 添加一个透明的背景颜色；  
>button-icon 没有边框

```java
<button class="button button-block button-positive">
  Block Button
</button>
////////////////////////////////
<button class="button icon-left ion-home">Home</button>
<button class="button icon-left ion-star button-positive">Favorites</button>
<a class="button icon-right ion-chevron-right button-calm">Learn More</a>
<a class="button icon-left ion-chevron-left button-clear button-dark">Back</a>
<button class="button icon ion-gear-a"></button>
<a class="button button-icon icon ion-settings"></a>
<a class="button button-outline icon-right ion-navicon button-balanced">Reorder</a>
///////////////////////////////////////
<div class="button-bar">
  <a class="button">First</a>
  <a class="button">Second</a>
  <a class="button">Third</a>
</div>
```
##List
应用很广泛，如：文本，按钮开关，图标，缩略图。。。  
它是一个强大的组建，如：编辑，滑动编辑，拖动排序，拉刷新等等。。。  
列表分割：使用item-divider可以创建分割，默认会有不同背景颜色以及字体加粗
，这个很容易定制。  
列表图标：使用item-icon-left和item-icon-right（父级）
item-note注释   badge徽章   （说默认有右箭头，没看到。。。。）  
列表按钮：item-button-right，可以在按钮里放Icon.    
项目头像：本质上讲，就是比图标大一点，小于说略图。使用.item-avatar


```java
<ul class="list">
    <li class="item">
      ...
    </li>
</ul>
//////////////////////////////////////
<div class="list">

  <div class="item item-divider">
    Candy Bars
  </div>

  <a class="item" href="#">
    Butterfinger
  </a>

  ...

</div>
/////////////////////////////////////////////////
<div class="list">

  <a class="item item-icon-left" href="#">
    <i class="icon ion-email"></i>
    Check mail
  </a>

  <a class="item item-icon-left item-icon-right" href="#">
    <i class="icon ion-chatbubble-working"></i>
    Call Ma
    <i class="icon ion-ios7-telephone-outline"></i>
  </a>

  <a class="item item-icon-left" href="#">
    <i class="icon ion-mic-a"></i>
    Record album
    <span class="item-note">
      Grammy
    </span>
  </a>

  <a class="item item-icon-left" href="#">
    <i class="icon ion-person-stalker"></i>
    Friends
    <span class="badge badge-assertive">0</span>
  </a>

</div>
/////////////////////////////////////////////////
<div class="list">

  <div class="item item-button-right">
    Call Ma
    <button class="button button-positive">
      <i class="icon ion-ios7-telephone"></i>
    </button>
  </div>
</div>
/////////////////////////////////////////////////////
<div class="list">

    <a class="item item-avatar" href="#">
      <img src="venkman.jpg">
      <h2>Venkman</h2>
      <p>Back off, man. I'm a scientist.</p>
    </a>
</div>
```
##Item Thumbnails   缩略图
缩略图本质上是展示的是比一个图标大一点。通常定义为整个列表的高。创建缩略图项目使用
item-thumbnails-left    item-thumbnails-right
```
<div class="list">
    <a class="item item-thumbnail-left" href="#">
      <img src="cover.jpg">
      <h2>Pretty Hate Machine</h2>
      <p>Nine Inch Nails</p>
    </a>
</div>
```

##Inset List
它可以嵌套在容器内，嵌套有点类似card，除了它没有box-shadow。它并不占有一个全屏宽度，
主要的不同是它有边距margin
```
<div class="list list-inset">
    <div class="item">
      Raiders of the Lost Ark
    </div>
</div>
```

##Cards
在近几年经被广泛的使用，它有非常好的方法包含和组织信息。在小屏幕上可以达到预期的效果，很快
被各大公司使用如google等企业。  
移动方面的经验：卡片很容易在不同屏幕上展示相同信息。有很多控制方式，灵活，甚至可以是
动画。虽然放在某些元素之上，但也可以像page一样安排在中间，左或者右边。  
卡片默认是有box-shadow与它的堂兄弟list-inset不同，处于性能上的考虑。当有大量的滚动卡片
效果，推荐使用插图列表！
```
<div class="card">
  <div class="item item-text-wrap">
    This is a basic Card which contains an item that has wrapping text.
  </div>
</div>
```
##Card Headers and Footers
卡片可以在正常的屏幕上定制相同的效果，例如：卡片可以很容易的放做header和footer内部，
也可以在content中用item-divider上定义分割线；
```
<div class="card">
  <div class="item item-divider">
    I'm a Header in a Card!
  </div>
  <div class="item item-text-wrap">
    This is a basic Card with some text.
  </div>
  <div class="item item-divider">
    I'm a Footer in a Card!
  </div>
</div>
```
##Card Lists
使用list card类名，可以创建一个卡片列表；
```
<div class="list card">
  <a href="#" class="item item-icon-left">
    <i class="icon ion-home"></i>
    Enter home address
  </a>
</div>
```
##Card Images 卡片图片
图片做卡片里很好用，也能很好的结合列表和其它元素。
```
<div class="list card">
  <div class="item item-avatar">
    <img src="avatar.jpg">
    <h2>Pretty Hate Machine</h2>
    <p>Nine Inch Nails</p>
  </div>

  <div class="item item-image">
    <img src="cover.jpg">
  </div>

  <a class="item item-icon-left assertive" href="#">
    <i class="icon ion-music-note"></i>
    Start listening
  </a>
</div>
```
##Forms 与 Inputs
列表也可以跟一组表单元素相关联，item-input  item用来指定每个输入字段于相关的标签！  
Ionic更推荐使用item-input，这样可以在row上的任意位置上触发焦点。  
除此之外，开发者也意识到H5表单类型，因此用户将会看到适当的虚拟键盘；


##Text Input:Placeholder Labels
默认会占用百分百的宽度没有左右边框，使用placeholder标签属性来模拟输入的标签。
当用户开始键入文本的时候，标签隐藏。反之~~~   
textarea可以使用多行文本表单；
```
<div class="list">
  <label class="item item-input">
    <input type="text" placeholder="First Name">
  </label>
  <label class="item item-input">
    <input type="text" placeholder="Last Name">
  </label>
  <label class="item item-input">
    <textarea placeholder="Comments"></textarea>
  </label>
</div>
```

##Text Input：Inline Labels
使用input-lable可以放置做input元素的左侧，当用户键入的时候它并不会消失。它不会
阻止你去使用一个占位符；
```
<div class="list">
  <label class="item item-input">
    <span class="input-label">Username</span>
    <input type="text">
  </label>
  <label class="item item-input">
    <span class="input-label">Password</span>
    <input type="password">
  </label>
</div>
```

##Text Input: Stacked Labels
堆叠标签：标签总是被放置做Input之上。每个项目都有item-stacked-label标签。
输入的标签上input-label。  
例如：还是可以使用placeholder去提示用户江湖要输入什么样子的文本类型；
```
<div class="list">
  <label class="item item-input item-stacked-label">
    <span class="input-label">First Name</span>
    <input type="text" placeholder="John">
  </label>
  <label class="item item-input item-stacked-label">
    <span class="input-label">Last Name</span>
    <input type="text" placeholder="Suhr">
  </label>
  <label class="item item-input item-stacked-label">
    <span class="input-label">Email</span>
    <input type="text" placeholder="john@suhr.com">
  </label>
</div>
```
##Text Input：Floating Lables
浮动标签看起来像堆叠标签，除了它存在动画。或者当用户键入的时候它会漂浮到上面。  
每一个项目都有item-floating-lable，表单标签将有一个input-label标识；
```
<div class="list">
  <label class="item item-input item-floating-label">
    <span class="input-label">First Name</span>
    <input type="text" placeholder="First Name">
  </label>
```

##Inset Forms 
在列表里，默认的是input会占用其父级的百分百的宽度。然而你可以使用list-inset或者
card去嵌套。card有box-shadow    list-inset没有box-shadow。除此之外如果父级有Padding,
它也给予一个嵌套的形式；
```
<div class="list list-inset">
  <label class="item item-input">
    <input type="text" placeholder="First Name">
  </label>
  <label class="item item-input">
    <input type="text" placeholder="Last Name">
  </label>
</div>
```
##Inset Input
使用list-inset可以嵌套做整个列表里，然后放置item-input-inset将嵌套一个input在一个独立的
list item 里面；放置一个按钮做旁边。

##Input Icons
图标可以很容易的加进item-input的Input里，简单的在Input之前加上icon。默认文本颜色跟
label颜色一致；但是你也可以使用placeholder-icon去修改成占位符的颜色！
```
<div class="list list-inset">
  <label class="item item-input">
    <i class="icon ion-search placeholder-icon"></i>
    <input type="text" placeholder="Search">
  </label>
</div>
```
##Header Inputs
表单也可以被安置做头部，跟随这提交按钮或者取消表单！
```
<div class="bar bar-header item-input-inset">
  <label class="item-input-wrapper">
    <i class="icon ion-ios7-search placeholder-icon"></i>
    <input type="search" placeholder="Search">
  </label>
  <button class="button button-clear">
    Cancel
  </button>
</div>
```

##Toggle
跟Html中的复选框切换都一样，除了看起不同。可以很容易的放在触摸设备上。Ionic
更喜欢在input外部放一个Label为了更好的切或者拖动；  
Toggle也能设计颜色，可以使用toggle-assertive
```
<label class="toggle">
   <input type="checkbox">
   <div class="track">
     <div class="handle"></div>
   </div>
</label>
```

##Checkbox
Checkbox跟Html里面的checkbox有一点不同，除了样式上的不同。
item-checkbox被加在item后面；Ionic喜欢做label里面加如checkbox，那样更有助于选中。  
它也是可以设置颜色的，需要使用checkbox-assertive
```
<ul class="list">
  <li class="item item-checkbox">
     <label class="checkbox">
       <input type="checkbox">
     </label>
     Flux Capacitor
  </li>
</ul>
```
##Radio Button List
单选按钮其实跟原生的并没有什么不同，每一个item-radio下的input里面必须有一个相同的
name  
radio-icon可以用来指定标识显示或者隐藏的元素。
```
<div class="list">
  <label class="item item-radio">
    <input type="radio" name="group">
    <div class="item-content">
      Go
    </div>
    <i class="radio-icon ion-checkmark"></i>
  </label>
</div>
```
##Range
Range是一个范围；range的主题可以是任意的一个ionic颜色。可以使用各种各样的元素，
列表项目或者卡片；
```
<div class="range">
  <i class="icon ion-volume-low"></i>
  <input type="range" name="volume">
  <i class="icon ion-volume-high"></i>
</div>

<div class="list">
  <div class="item range range-positive">
    <i class="icon ion-ios7-sunny-outline"></i>
    <input type="range" name="volume" min="0" max="100" value="33">
    <i class="icon ion-ios7-sunny"></i>
  </div>
</div>
```
##Select
Ionic的多选相比比浏览器漂亮些，是根据浏览器选择的。默认的行为还是根据浏览器有关。
不同平台展示效果是不同的，例如：桌面浏览器就是一个向下的弹出框。安卓有一组单选的按钮组
ios将出现一个照片卷轴一样的覆盖半个屏幕。
```
<div class="list">
  <label class="item item-input item-select">
    <div class="input-label">
      Lightsaber
    </div>
    <select>
      <option>Blue</option>
      <option selected>Green</option>
      <option>Red</option>
    </select>
  </label>
</div>
```
##Tabs
Tabs是一组水平的按钮或链接,在各浏览器都有一致的体验。它可以包含文本和图标。使得
在移动端是非常浏览的导航；元素应该包含一个tabs,每一个tab都将包含一个tab-item默认
没有图标只有一个文本；Tabs可以匹配标准的ionic颜色。  
如果tabbar隐藏了，还显示内容。可以添加一个tabs-item-hide类。或者当你使用的时候记得加
has-tabs类。
```
<div class="tabs">
  <a class="tab-item">
    Home
  </a>
  <a class="tab-item">
    Favorites
  </a>
  <a class="tab-item">
    Settings
  </a>
</div>
```
##Ioon-only Tabs
在tabs后添加tabs-icon-only类
```
<div class="tabs tabs-icon-only">
  <a class="tab-item">
    <i class="icon ion-home"></i>
  </a>
  <a class="tab-item">
    <i class="icon ion-star"></i>
  </a>
  <a class="tab-item">
    <i class="icon ion-gear-a"></i>
  </a>
</div>
```
##Top Icon Tabs
在tabs添加tabs-icon-top类
```
<div class="tabs tabs-icon-top">
  <a class="tab-item">
    <i class="icon ion-home"></i>
    Home
  </a>
  <a class="tab-item">
    <i class="icon ion-star"></i>
    Favorites
  </a>
  <a class="tab-item">
    <i class="icon ion-gear-a"></i>
    Settings
  </a>
</div>
```
##Left Icon Tabs
在tabs后添加tabs-icon-left
```
<div class="tabs tabs-icon-left">
  <a class="tab-item">
    <i class="icon ion-home"></i>
    Home
  </a>
  <a class="tab-item">
    <i class="icon ion-star"></i>
    Favorites
  </a>
  <a class="tab-item">
    <i class="icon ion-gear-a"></i>
    Settings
  </a>
</div>
```
##Striped Style Tabs
在tabs上添加tabs-striped具有安卓风格，也可以使用类名tabs-top定位做顶部。获取angular   Striped tabs
背景颜色用tabs-background-{color}，字体颜色tabs-color-{color}
它于头部怕混合使用，这个时候要添加has-tabs-top类。以流出头部间距。
```
<div class="tabs-striped tabs-top tabs-background-positive tabs-color-light">
    <div class="tabs">
      <a class="tab-item active" href="#">
        <i class="icon ion-home"></i>
        Test
      </a>
      <a class="tab-item" href="#">
        <i class="icon ion-star"></i>
        Favorites
      </a>
      <a class="tab-item" href="#">
        <i class="icon ion-gear-a"></i>
        Settings
      </a>
    </div>
  </div>
  <div class="tabs-striped tabs-color-assertive">
    <div class="tabs">
      <a class="tab-item active" href="#">
        <i class="icon ion-home"></i>
        Test
      </a>
      <a class="tab-item" href="#">
        <i class="icon ion-star"></i>
        Favorites
      </a>
      <a class="tab-item" href="#">
        <i class="icon ion-gear-a"></i>
        Settings
      </a>
    </div>
  </div>
  ```
##Toggle
和HTML中的复选框切换都一样，除了看起来不一样。做触摸设备上很容易使用。 
在label中使用会更好的切换Toggle；  
也可以分配颜色给它们，如toggle-assertive；也可以做为多列表，将item-toggle
放在没一个Item里面；
```
<ul class="list">
  <li class="item item-toggle">
     HTML5
     <label class="toggle toggle-assertive">
       <input type="checkbox">
       <div class="track">
         <div class="handle"></div>
       </div>
     </label>
  </li>
</ul>
```
##Checkbox
它和HTML中的并没有什么不同，除了样式看起来不同。可以做一个checkboxes多列~~在
每一个item中放入一个item-checkbox；  
ionic提供了<label>，这样使用它更容易。checkboxes也可以分配颜色给他们。如加入checkbox-assertive；
```
<ul class="list">
  <li class="item item-checkbox">
     <label class="checkbox">
       <input type="checkbox">
     </label>
     Flux Capacitor
  </li>
</ul>
```
##Radio Button List
单选按钮跟标准的单选按钮并没有什么不同，除了样式上有所不同。
每一个item-radio不得不有一个相同的Name属性；radio-icon也是可以被指派的。去 
显示或者隐藏一个图标元素；ionic提供<label>使得用起来更容易，可以做全屏上触摸；
```
<div class="list">
  <label class="item item-radio">
    <input type="radio" name="group">
    <div class="item-content">
      Go
    </div>
    <i class="radio-icon ion-checkmark"></i>
  </label>
</div>
```
##Range
这是一个值域,颜色可以定义为任何默认的Ionic颜色；可以使用多种元素，如列表或者卡片；
```
<div class="range">
  <i class="icon ion-volume-low"></i>
  <input type="range" name="volume">
  <i class="icon ion-volume-high"></i>
</div>

<div class="list">
  <div class="item range range-positive">
    <i class="icon ion-ios7-sunny-outline"></i>
    <input type="range" name="volume" min="0" max="100" value="33">
    <i class="icon ion-ios7-sunny"></i>
  </div>
</div>
```
##Select
Ionic的多选相比，比浏览器漂亮些；当选择开始时，默认行为如何选择其中一个选项仍然是由
浏览器。用户选择一个选项，每个平台的用户界面会有所不同。做桌面浏览器显示默认下
拉框，Android会有单选框列表弹出，Ios有自定义照片卷轴窗口遮盖窗口的下半部；
```
<div class="list">
  <label class="item item-input item-select">
    <div class="input-label">
      Lightsaber
    </div>
    <select>
      <option>Blue</option>
      <option selected>Green</option>
      <option>Red</option>
    </select>
  </label>
</div>
```
##Tabs
一组水平组合的按钮或者链接，它能包含任何组成部分，做移动端很受欢迎的导航！
包含元素有一个tabs类名，每个tab都有一个tab-item类名。默认没有图标仅仅是文本；
一样是可以有多种颜色可以进行更改；  
隐藏tabbar但仍然显示内容，添加tabs-item-hide类；  
当然如果你使用tabs也可以加has-tabs类。
```
<div class="tabs">
  <a class="tab-item">
    Home
  </a>
  <a class="tab-item">
    Favorites
  </a>
  <a class="tab-item">
    Settings
  </a>
</div>
```
##Icon-only
在tabs后加tabs-icon-only
```
<div class="tabs tabs-icon-only">
  <a class="tab-item">
    <i class="icon ion-home"></i>
  </a>
  <a class="tab-item">
    <i class="icon ion-star"></i>
  </a>
  <a class="tab-item">
    <i class="icon ion-gear-a"></i>
  </a>
</div>
```
##Top Icon Tabs
添加tabs-icon-top在tabs
```
<div class="tabs tabs-icon-top">
  <a class="tab-item">
    <i class="icon ion-home"></i>
    Home
  </a>
  <a class="tab-item">
    <i class="icon ion-star"></i>
    Favorites
  </a>
  <a class="tab-item">
    <i class="icon ion-gear-a"></i>
    Settings
  </a>
</div>
```
##Left Icon Tabs
在tabs后添加tabs-icon-left
```
<div class="tabs tabs-icon-left">
  <a class="tab-item">
    <i class="icon ion-home"></i>
    Home
  </a>
  <a class="tab-item">
    <i class="icon ion-star"></i>
    Favorites
  </a>
  <a class="tab-item">
    <i class="icon ion-gear-a"></i>
    Settings
  </a>
</div>
```
##Striped Style
在tabs外有一个tabs-striped，可做出Android风格。加Tabs-top可以定位top，可控制颜色；
tabs-background-{color}控制背景色，tabs-color-{color} 控制字体颜色；  
顶部tabs与头部混合，需要使用has-tabs-top类名；
```
<div class="tabs-striped tabs-top tabs-background-positive tabs-color-light">
    <div class="tabs">
      <a class="tab-item active" href="#">
        <i class="icon ion-home"></i>
        Test
      </a>
      <a class="tab-item" href="#">
        <i class="icon ion-star"></i>
        Favorites
      </a>
      <a class="tab-item" href="#">
        <i class="icon ion-gear-a"></i>
        Settings
      </a>
    </div>
</div>
<div class="tabs-striped tabs-color-assertive">
    <div class="tabs">
      <a class="tab-item active" href="#">
        <i class="icon ion-home"></i>
        Test
      </a>
      <a class="tab-item" href="#">
        <i class="icon ion-star"></i>
        Favorites
      </a>
      <a class="tab-item" href="#">
        <i class="icon ion-gear-a"></i>
        Settings
      </a>
    </div>
</div>
```
##Grid
Ionic网格系统不大相同，因为它是用 CSS Flexible Box Layout Module标准；优势在于支持
Ionic的设备都支持 flexbox；  
简单的添加行与列：它们会均匀的占用可用空间。如果你想建立一个三行就三行，五列就五列；
这里不限制使用那个12网格。或者不需要明确状态。你可以垂直的对齐做每一列的内容；
使用row惊醒指定，去支持一行。使用col去指定一列。想怎么加就怎么加，不用多想，它会自动编译的；
##Grid：Evenly Spaced Columns
默认做col里面添加row将会自动获取等量的间距，在样式内部不指定任何的大小；
##Grid:Explicit Column Sizes
你可以明确一个单元格的大小，如何你想指定某个单元格比其他它的大想同一行里。默认的是
他们都会有相同的指定有效空间。Ionic使用的网格系统是百分比（相比一个锁定12列网格）
这种网格系统的优势是，你仅仅做你需要的地方设置百分百。其它的仍然可以分割剩余的空间；
```
<div class="row">
  <div class="col col-50">.col.col-50</div>
  <div class="col">.col</div>
  <div class="col">.col</div>
</div>

<div class="row">
  <div class="col col-75">.col.col-75</div>
  <div class="col">.col</div>
</div>

<div class="row">
  <div class="col">.col</div>
  <div class="col col-75">.col.col-75</div>
</div>

<div class="row">
  <div class="col">.col</div>
  <div class="col">.col</div>
</div>
```
Explicit Column Percentage Classnames

* .col-10   10%

* .col-20 	20%

* .col-25 	25%

* .col-33 	33.3333%

* .col-50 	50%

* .col-67 	66.6666%

* .col-75 	75%
 
* .col-80 	80%

*.col-90 	90%

##Grid: Offset Columns
单元格可以从左侧开始偏；
```
<div class="row">
  <div class="col col-33 col-offset-33">.col</div>
  <div class="col">.col</div>
</div>

<div class="row">
  <div class="col col-33">.col</div>
  <div class="col col-33 col-offset-33">.col</div>
</div>

<div class="row">
  <div class="col col-33 col-offset-67">.col</div>
</div>
```
Offset Column Percentage Classnames 

* .col-offset-10 10%

* .col-offset-20 	20%

* .col-offset-25 	25%

* .col-offset-33 	33.3333%

* .col-offset-50 	50%

* .col-offset-67 	66.6666%

* .col-offset-75 	75%

* .col-offset-80 	80%

* .col-offset-90 	90%

##Grid: Vertically Align Columns
另一个技巧flexbox的套筒是能够轻易列垂直对齐,对齐包括上、中、下。可以应用的每一行的一列，
或者特定的一列。
```
<div class="row">
  <div class="col">.col</div>
  <div class="col">.col</div>
  <div class="col">.col</div>
  <div class="col">1<br>2<br>3<br>4</div>
</div>

<div class="row">
  <div class="col col-top">.col</div>
  <div class="col col-center">.col</div>
  <div class="col col-bottom">.col</div>
  <div class="col">1<br>2<br>3<br>4</div>
</div>

<div class="row row-top">
  <div class="col">.col</div>
  <div class="col">.col</div>
  <div class="col">.col</div>
  <div class="col">1<br>2<br>3<br>4</div>
</div>

<div class="row row-center">
  <div class="col">.col</div>
  <div class="col">.col</div>
  <div class="col">.col</div>
  <div class="col">1<br>2<br>3<br>4</div>
</div>

<div class="row row-bottom">
  <div class="col">.col</div>
  <div class="col">.col</div>
  <div class="col">.col</div>
  <div class="col">1<br>2<br>3<br>4</div>
</div>
```
##Responsive Grid
或许可能出这样的现象，执行一行将不会非常适合到可选的区域；相应类可以在一行里应用；
例如：你想将一行栏做成堆栈的，当试图非常小可以使用.responsive-sm类。  
进一步配置，每个类使用sass变量。可根据你的喜欢改变。可以使用responsive-grid-break混入类
来创建自己的类；
Responsive Class     Break when roughly

* .responsive-sm 	Smaller than landscape phone

* .responsive-md 	Smaller than portrait tablet

* .responsive-lg 	Smaller than landscape tablet
