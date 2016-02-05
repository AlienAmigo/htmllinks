---
layout: post
title: Оптимизация графики для Retina-экранов
category: guides, articles,
tags: retina, графика, изображение, картинка, фотография,
link: http://habrahabr.ru/post/150071/
description:
keywords:
---

<p>Хорошая статья, объясняющая как готовить графику для retina-экранов (экраны с большой плотностью пикселей). Как и всегда на Хабре, обязательно нужно читать комментарии. Особенно — самый первый.</p>
<div class="panel panel-code"><div class="panel-heading"><p class="panel-title"><a href="#collapse_195" data-toggle="collapse" class="local-link">В чем соль? Коротко
</a></p></div><div class="panel-collapse collapse" id="collapse_195"><div class="panel-body">
<p>Правильно писать @media-конструкцию для экранов с большой плотностью пикселей так:</p>
<pre><span class="at_rule">@<span class="keyword">media</span> only screen and (-webkit-min-device-pixel-ratio: <span class="number">1.5</span>)
       only screen and (min-resolution: <span class="number">144</span>dpi) </span>{ ... }
</pre>
</div></div></div>
