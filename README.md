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