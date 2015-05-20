
- **jquery 实战**
- 
>jquery($)包装DOM对象，所有的jq方法都可以直接作用在最初的选择器上，一层层作用

>window.onload=function(){} 加载完DOM结构+外部资源（图片、flash）执行

>$(function(){})  加载完DOM结构执行

>jquery插件扩展法：

```javascript
$.fn.disable=function(){
  return this.each(function(){
    if(this.disabled!=null)
    this.disabled=true
  })
}
调用：$('id').disable().addClass('a')
```
选择器类型

```javascript

  $('p:even')
  $('body>div')
  $('body>div:has(a)')
  ——————
  a[href$='http:/']
  $:
  ^:
  !:
  *:
  _______
  伪类/过滤器：
  ：first
  :even
  :eq(n)
  :gt(n)
  :ln(n)
  _______
  自定义选择器
  ：animated
  :button
  :not(selector)
  :has(selector)
  eq:
  :checkbox:checked:enabled
  input:not(:checkbox)
  $('img:not([src*='dog'])')
  $('tr:has(img[src$="a"])')
  
```

```javascript
  $('<img>',
  {
    src:'a.png',
    alt:'nihao',
    click:function(){
      $(htis).attr('title')
    }
  }
  ).css({
    border:'1px solid red'
  }).appendTo('body')
```
包装集
```javasrcipt
$('a').size()
eq(index)
first()
last()
toArray()
index()
add()
$('img[alt]').addd('img[title]')
$('img').not(function(){
  return !$(this).has('a')
})
$('img').addClass('a').filter('[title*=a]').addClass('a')
$('img[title]').not('[title*=a]')
```
-------------------

