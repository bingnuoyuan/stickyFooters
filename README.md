> 在网页设计中，Sticky footers设计是最古老和最常见的效果之一，大多数人都曾经经历过。它可以概括如下：如果页面内容不够长的时候，页脚块粘贴在视窗底部；如果内容足够长时，页脚块会被内容向下推送。


###  解决方案
1. 固定高度的解决方案

> html布局
```
<header>
    <h1>Site name</h1> 
</header> 
<main> 
    <p>
    Bacon Ipsum dolor sit amet...
    <!-- Filler text from baconipsum.com -->
    </p> 
</main> 
<footer> 
<p>© 2015 No rights reserved.</p> 
<p>Made with ♥ by an anonymous </p>
</foter>
```

> css样式

```
main {
    min-height: calc(100vh - 2.5em - 7em); 
    /* Avoid padding/borders screwing up our height: */ 
    box-sizing: border-box;
}
```

2.使用flexbox布局

> html布局
```
<header>
    <h1>Site name</h1> 
</header> 
<main> 
    <p>
    Bacon Ipsum dolor sit amet...
    <!-- Filler text from baconipsum.com -->
    </p> 
</main> 
<footer> 
<p>© 2015 No rights reserved.</p> 
<p>Made with ♥ by an anonymous </p>
</foter>
```

> css样式

```
body { 
    display: flex;
    flex-flow: column;
    min-height: 100vh;
}
main { 
    flex: 1 0 auto;
}
```

