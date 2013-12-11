bliss
=====

(beautifully lean, ideal style sheets)

bliss is a CSS experiment.

author: [@chrisnager](http://twitter.com/chrisnager)

---

_bliss takes the entire CSS language and splits each declaration into single purpose Sass placeholders_.

```scss
%text-align_center { text-align: center; }

.header-bar {
    @extend text-align_center;
}
```

_bliss allows your markup to stay perfectly clean_, one class per styled element. Sass placeholders allow you to build your CSS modularly.

```markup
    <div class="header-bar">App Title</div>
```

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

_bliss is performant_. It only compiles the CSS that is used so your style sheet stays lean.

To take full advantage of bliss you must [minify your CSS](http://www.minifycss.com/css-compressor/).

---

Shoutout to my west coast friends:
I came up with the idea for bliss at six in the morning while chillin' with [@jina](http://twitter.com/jina) and [@mrmrs](http://twitter.com/mrmrs) chatting all night about CSS.


