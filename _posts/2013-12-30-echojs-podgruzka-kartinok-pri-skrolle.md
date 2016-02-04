---
layout: post
title: Echo.js — подгрузка картинок при скролле
category: recipes-javascript, manuals, 
tags: javascript, lazy-loading, загрузка, изображение, картинка, подгрузка, прокрутка, скролл, 
link: http://toddmotto.com/labs/echo/
description: 
keywords: 
---

<p>Принцип lazy loading — это подгрузка контентных изображений только в том случае, если посетитель «докрутил» скролл до того места, где расположена картинка. Подключаем этот JS и пишем вместо контентных картинок:</p>

<pre lang=html>&lt;img src=&quot;img/blank.gif&quot; alt=&quot;&quot; data-echo=&quot;img/album-1.jpg&quot;&gt;</pre>
<p>Не требует к-л фреймворков.</p>
