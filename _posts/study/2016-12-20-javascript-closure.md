---
layout: post
title:  JavaScript 闭包
date:   2016-12-20
categories: study
tags: [JavaScript]
---

一个闭包在创建时会附有三个属性：VO、thisValue、scope chain，而其中scope chain是指向外层parent scope的引用。

``` javascript
for(var i = 0; i < 10; i++) {
    setTimeout(function() {
        console.log(i);
    }, 1000);
}
//运行结果： 一秒后输出十次10
```

当`console.log`被调用的时候，匿名函数保持对外部变量`i`的引用，此时`for`循环已经结束，`i`的值被修改成了`10`。

为了输出数字 0~9，需要在每次循环中创建变量`i`的拷贝，避免引用错误。

``` javascript
for(var i = 0; i < 10; i++) {
    setTimeout((function(e) {
        console.log(e);
    })(i), 1000);
}
//运行结果： 一次性输出0~9
```
