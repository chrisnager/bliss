bliss
=====

beautifully lean, ideal style sheets

bliss is a CSS experiment by [@chrisnager](http://twitter.com/chrisnager)


---


__bliss takes the entire CSS language and splits each declaration into single purpose Sass placeholders__.

```scss
%text-align_center { text-align: center; }

.header-bar {
    @extend text-align_center;
}
```


__bliss allows your markup to stay perfectly clean__, one class per styled element.

```html
<div class="header-bar">App Title</div>
```


Sass placeholders allow you to build your CSS modularly.

```scss
%section {
    @extend %padding_m;
    @extend %background-color_silver;
}

.header-bar {
    @extend section;
    @extend text-align_center;
}
```


__bliss is performant__. It only compiles the CSS that is used so your style sheet stays lean.

_To take full advantage of bliss you should [optimize](http://bem.info/tools/optimizers/csso/) your CSS_.


---


__References__

https://developer.mozilla.org/en-US/docs/Web/CSS/Reference


---


Shoutout to my west coast friends:
I came up with the idea for bliss at six in the morning while chillin' with [@jina](http://twitter.com/jina) and [@mrmrs_](http://twitter.com/mrmrs_) chatting all night about CSS.
