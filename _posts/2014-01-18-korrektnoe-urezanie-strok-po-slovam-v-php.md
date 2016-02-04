---
layout: post
title: Корректное урезание строк по словам в PHP
category: recipes-php, manuals, 
tags: обрезание, обрезка, подрезка, слово, функция, 
link: http://maxsite.org/page/korrektnoe-urezanie-strok-po-slovam-v-php
description: 
keywords: 
---

<p>Функция для корректного урезания текста по словам. Нет проблем с UTF8.</p>
<div class="panel panel-code"><div class="panel-heading"><p class="panel-title"><a href="#collapse_64" data-toggle="collapse" class="local-link">Листинг
</a></p></div><div class="panel-collapse collapse" id="collapse_64"><div class="panel-body">
<pre>
function maxsite_str_word($text, $counttext = 10, $sep = ' ') {
    $words = split($sep, $text);
    if ( count($words) > $counttext )
        $text = join($sep, array_slice($words, 0, $counttext));
    return $text;
}
</pre>
</div></div></div>
