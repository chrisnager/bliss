![bliss](bliss.png "bliss")

# *bliss*

beautifully lean, ideal style sheets

*bliss* is a CSS experiment by [@chrisnager](http://twitter.com/chrisnager)


---


__*bliss* includes the entire CSS language and splits each declaration into single purpose Sass placeholders__.

```scss
%text-align_left {
    text-align: left;
}

%text-align_right {
    text-align: right;
}

%text-align_center {
    text-align: center;
}

%text-align_justify {
    text-align: justify;
}
…
```


Feel free to add more as you see fit and put them in a file called `_author_variables.scss`.

```scss
%font-size_jumbo {
    font-size: 8rem;
}
```


__*bliss* allows your markup to stay perfectly clean__, one class per styled element.

```html
<div class="header-bar">…</div>
```


Sass placeholders allow you to build your CSS modularly.

```scss
// Single purpose Sass placeholders
%padding_m {
    padding: 1rem;
}

%background-color_silver {
    background-color: silver;
}

%text-align_center {
    text-align: center;
}



// Author's custom placeholder modules
%bar {
    @extend %padding_m;
    @extend %background-color_silver;
}



// Author's custom class modules
.header-bar {
    @extend %bar;
    @extend %text-align_center;
}
```


__*bliss* is performant__. It only compiles the CSS that is used so your style sheet stays lean.

```css
.header-bar {
    padding: 1rem;
    background-color: silver;
    text-align: center;
}
```


_To take full advantage of *bliss* you should optimize your CSS with a tool like [CSSO](http://bem.info/tools/optimizers/csso/)_.


---


__References__

https://developer.mozilla.org/en-US/docs/Web/CSS/Reference


---


Shoutout to my west coast friends:
I came up with the idea for *bliss* at six in the morning while chillin' with [@jina](http://twitter.com/jina) and [@mrmrs_](http://twitter.com/mrmrs_) chatting all night about CSS.

