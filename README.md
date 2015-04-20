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