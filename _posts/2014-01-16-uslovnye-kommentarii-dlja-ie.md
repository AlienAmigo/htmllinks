---
layout: post
title: Условные комментарии для IE
category: reference, guides
tags: conditional comments, internet explorer, microsoft, баг, браузер, условные комментарии, хак
link: http://designformasters.info/posts/conditional-comments/
description:
keywords:
---

<p>Статья 2008 года для тех, кто верстает для Internet explorer 9 и более старых (начиная с 10-й версии, условные комментарии не работают).</p>
<div class="panel panel-code"><div class="panel-heading"><p class="panel-title"><a href="#collapse_64" data-toggle="collapse" class="local-link">В чем соль? Коротко
</a></p></div><div class="panel-collapse collapse" id="collapse_64"><div class="panel-body">
<p>В html можно вписать конструкции, код в которых будет виден (будет отрабатывать) только в IE или во всех браузерах кроме IE. Так можно добавлять классы к тегу html, подключать отдельные таблицы стилей для конкретных версий IE и пр.</p>
<pre>&lt;!--[if IE]&gt;&lt;![if !IE]&gt;&lt;![endif]--&gt; <br style="clear:both">&lt;p&gt;Текст для любого браузера кроме IE&lt;/p&gt; <br style="clear:both">&lt;!--[if IE]&gt;&lt;![endif]&gt;&lt;![endif]--&gt;</p>
<p>&lt;!--[if IE]&gt;&lt;![if gte IE7]&gt;&lt;![endif]--&gt; <br style="clear:both">&lt;p&gt;Текст для любого браузера и IE 7+&lt;/p&gt; <br style="clear:both">&lt;!--[if IE]&gt;&lt;![endif]&gt;&lt;![endif]--&gt;</p>
<p>&lt;!-- в общем, методология такая: --&gt;</p>
<p>&lt;!--[if условие]&gt; HTML &lt;![endif]--&gt; <br style="clear:both">&lt;![if условие]&gt; HTML &lt;![endif]&gt;</p>
<p>&lt;!--[if IE]&gt;&lt;p&gt;Текст для любой версии IE&lt;/p&gt;&lt;![endif]--&gt; <br style="clear:both">&lt;!--[if IE 6]&gt;&lt;p&gt;Текст для IE 6&lt;/p&gt;&lt;![endif]--&gt; <br style="clear:both">&lt;!--[if IE 7]&gt;&lt;p&gt;Текст для IE 7&lt;/p&gt;&lt;![endif]--&gt;</pre>
<table class="table  table-bordered  table-responsive">
<tbody><tr><th >Элемент</th><th >Пример</th><th style="text-align: center;">Значение</th></tr>
<tr><td >IE</td><td >[if IE]</td><td>Единственное поддерживаемое сейчас свойство IE, равное версии Internet Explorer.</td></tr>
<tr><td >value</td><td >[if IE 7]</td><td>Целое или дробное число обозначающее версию браузера. Выражение истинно если число совпадает с версией браузера. </td></tr>
<tr><td >!</td><td >[if !IE]</td><td>Оператор отрицания. Возвращает значение обратное логическому значению аргумента.</td></tr>
<tr><td >lt</td><td >[if lt IE 5.5]</td><td>Меньше. Возвращает true если первый аргумент меньше второго.</td></tr>
<tr><td >lte</td><td >[if lte IE 6]</td><td>Меньше либо равно. Возвращает true если первый аргумент меньше либо равен второму.</td></tr>
<tr><td >gt</td><td >[if gt IE 5]</td><td>Больше. Возвращает true если первый аргумент больше второго.</td></tr>
<tr><td >gte</td><td >[if gte IE 7]</td><td>Больше либо равно. Возвращает true если первый аргумент больше либо равен второму.</td></tr>
<tr><td >( )</td><td >[if !(IE 7)]</td><td>Скобки позволяют выделить подвыражения в сложном выражении. </td></tr>
<tr><td >&</td><td ><span style="white-space:nowrap;">[if (gt IE 5)&(lt IE 7)]</span></td><td>Оператор AND. Возвращает true если оба подвыражения истинны.</td></tr>
<tr><td >|</td><td >[if (IE 6)|(IE 7)]</td><td>Оператор OR. Возвращает true если одно их подвыражений истинно.</td></tr>
</tbody></table>
</div></div></div>
