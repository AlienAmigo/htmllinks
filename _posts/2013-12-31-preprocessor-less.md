---
layout: post
title: Препроцессор LESS
category: less, preprocessors, 
tags: CSS, less, препроцессор, 
link: http://lesscss.org/
description: 
keywords: 
---

<p>Препроцессор LESS — простой в освоении язык, преобразуемый в CSS. Добавляет в работу с CSS переменные, вложения, примеси, математические операции, преобразования цветов, циклы, условия. Может работать на стороне сервера (компилироваться в CSS) и на стороне клиента (в этом случае, может содержать вставки JS).</p>
<div class="panel panel-code"><div class="panel-heading"><p class="panel-title"><a href="#collapse_1" data-toggle="collapse" class="local-link collapsed">
	Пример использования LESS
</a></p></div><div class="panel-collapse collapse" id="collapse_1" style="height: 0px;"><div class="panel-body">
<pre>// LESS
@base-font-size: 12px;

#header {
  h1 {
    font-size: @base-font-size * 2;
    font-weight: bold;
  }
  p { font-size: @base-font-size;
    a { text-decoration: none;
      &:hover { border-width: 1px }
    }
  }
}</pre>
<p>Будет скопмилировано в:</p> 
<pre>/* CSS */

#header h1 {
  font-size: 24px;
  font-weight: bold;
}
#header p {
  font-size: 12px;
}
#header p a {
  text-decoration: none;
}
#header p a:hover {
  border-width: 1px;
}</pre>
</div></div></div>
