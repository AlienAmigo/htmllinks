---
layout: post
title: Шрифты для Web
category: services, fonts
tags: font, шрифт
link: http://www.google.com/fonts/
description:
keywords:
---

<p>Подключение с сервиса (можно и скачать), настройки при подключении (можно получить ссылку на шрифт, содержащий только необходимые символы), отличный фильтр по шрифтам.</p>
<div class="hide panel panel-code"><div class="panel-heading"><p class="panel-title"><a class="local-link" data-toggle="collapse" href="#collapse_1">
	Как ускорить загрузку шрифтов с Google fonts примерно в два раза
</a></p></div><div id="collapse_1" class="panel-collapse collapse"><div class="panel-body">

<p>Есть в документации Гугла <a href="https://developers.google.com/fonts/docs/getting_started?hl=ru&csw=1#Optimizing_Requests" title="">любопытный раздел</a>, который как бы намекает нам: можно получить не весь шрифт, а только отдельные его символы. Значит, можно получить только кириллические символы какого-либо шрифта:</p>
<pre class="prettyprint linenums">/* CSS */
@import url('http://fonts.googleapis.com/css?family=Ubuntu:400,500&text=%D0%90%D0%91%D0%92%D0%93%D0%94%D0%95%D0%81%D0%96%D0%97%D0%98%D0%99%D0%9A%D0%9B%D0%9C%D0%9D%D0%9E%D0%9F%D0%A0%D0%A1%D0%A2%D0%A3%D0%A4%D0%A5%D0%A6%D0%A7%D0%A8%D0%A9%D0%AA%D0%AB%D0%AC%D0%AD%D0%AE%D0%AF%D0%B0%D0%B1%D0%B2%D0%B3%D0%B4%D0%B5%D1%91%D0%B6%D0%B7%D0%B8%D0%B9%D0%BA%D0%BB%D0%BC%D0%BD%D0%BE%D0%BF%D1%80%D1%81%D1%82%D1%83%D1%84%D1%85%D1%86%D1%87%D1%88%D1%89%D1%8A%D1%8B%D1%8C%D1%8D%D1%8E%D1%8F0123456789%20%21%40%23%24%25%5E%26%2A%28%29_%2B%C2%AB%C2%BB%E2%80%94%C3%97%C2%A9%3C%3E%2C.%2F%7C%5C%7B%7D%5B%5D%27%22%3B%3A%E2%84%96%25%3F-%C2%B1%3D');
</pre>
<p>Эта конструкция импортирует в ваш CSS‑файл <a href="http://www.google.com/fonts/specimen/Ubuntu" title="">шрифт Ubuntu</a>, плотность начертаний 400 и 500, включающий следующие символы:</p>
<pre>АБВГДЕЁЖЗИЙКЛМНОПРСТУФХЦЧШЩЪЫЬЭЮЯабвгдеёжзийклмнопрстуфхцчшщъыьэюя0123456789 !@#$%^&*()_+«»—×©<>,./|\{}[]'";:№%?-±=
</pre>
<p>Только кириллица, <del>только хардкор</del>, цифры, знаки, пробел.</p>
</div></div></div>
