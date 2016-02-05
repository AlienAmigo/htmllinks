---
layout: post
title: Головокружительное погружение в БЭМ
category: guides, articles
tags: css, бэм, имя, селектор
link: http://frontender.info/MindBEMding/#golovokruzhitelynoe-pogruzhenie-v-bm
description:
keywords:
---

<p>Превосходная статья о методологии БЭМ в разрезе именования CSS-селекторов.</p>
<p>Настоятельно рекомендуется к ознакомлению и использованию.</p>
<div class="panel panel-code"><div class="panel-heading"><p class="panel-title"><a href="#collapse_196" data-toggle="collapse" class="local-link">Что за метод именования css-селекторов?
</a></p></div><div class="panel-collapse collapse" id="collapse_196"><div class="panel-body">
<p>Система именования использует такой шаблон:</p>

<pre><code class="css"><span class="class">.block</span><span class="rules">{<span class="rule">}</span></span>
<span class="class">.block__element</span><span class="rules">{<span class="rule">}</span></span>
<span class="class">.block--modifier</span><span class="rules">{<span class="rule">}</span></span>
</code></pre>

<ul>
<li>
<code>.block</code> — самый высокий уровень абстракции компонента.</li>
<li>
<code>.block__element</code> — дочерний элемент <code>.block</code> помогающий поддерживать его целостность.</li>
<li>
<code>.block--modifier</code> — другое состояние или версия <code>.block</code>.</li>
</ul>
<p>Двойные символы используются вместо одиночных из-за того, что класс может быть
сам по себе разделён дефисом.</p>
</div></div></div>
