---
layout: post
title: Использование rem в CSS
category: guides, articles
tags: less, rem, sass, scss, stylus
link: http://alwaystwisted.com/post.php?s=2014-01-01-rems-fallbacks-and-support
description:
keywords:
---

<p>Статья об использовании единиц измерения rem в верстке. Приведены способы использования вместе с препроцессорами.</p>
<div class="panel panel-code"><div class="panel-heading"><p class="panel-title"><a href="#collapse_172" data-toggle="collapse" class="local-link">Что там с препроцессорами?..
</a></p></div><div class="panel-collapse collapse" id="collapse_172"><div class="panel-body">
<h3 id="LESS">LESS</h3>
<pre><code>/* Set up a variable for maths */

@doc-font-size: 16;

/* the font-size mixin */

.font-size (@size) {
  font-size: 0px + @size;
  font-size: 0rem + @size / @doc-font-size;
}

/* example of usage */

.prose p {
  .font-size(16);
}

/* example compiled */

.prose p {
  font-size: 16px;
  font-size: 1rem;
}</code></pre>
<h3 id="Sass">Sass(SCSS)</h3>
<pre><code>/* Set up a variable for maths */

$doc-font-size: 16;

/* the font-size mixin */

@mixin font-size($size) {
  font-size: 0px + $size;
  font-size: 0rem + $size / $doc-font-size;
}

/* example of usage */

.prose p {
  @include font-size(16);
}

/* example compiled */

.prose p {
  font-size: 16px;
  font-size: 1rem;
}</code></pre>
<h3 id="Stylus">Stylus</h3>
<pre><code>/* Set up a variable for maths */

doc-font-size = 16

/* the font-size mixin */

font-size(size)
  font-size: 0px + size
  font-size: 0rem + (size / doc-font-size)

/* example of usage */

.prose p
  font-size(16)

/* example compiled */

.prose p {
  font-size: 16px;
  font-size: 1rem;
}</code></pre>
</div></div></div>
