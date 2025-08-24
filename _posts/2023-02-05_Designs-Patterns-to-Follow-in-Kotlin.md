---
layout: post
title: "Design Patterns to Follow in Kotlin"
date: 2023-02-05
categories: kotlin
tags: [design-patterns, software, kotlin]
---

<!DOCTYPE html><html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"><title>Design Patterns to Follow in Kotlin: A Guide to Better Code</title><style>
      * {
        font-family: Georgia, Cambria, "Times New Roman", Times, serif;
      }
      html, body {
        margin: 0;
        padding: 0;
      }
      h1 {
        font-size: 50px;
        margin-bottom: 17px;
        color: #333;
      }
      h2 {
        font-size: 24px;
        line-height: 1.6;
        margin: 30px 0 0 0;
        margin-bottom: 18px;
        margin-top: 33px;
        color: #333;
      }
      h3 {
        font-size: 30px;
        margin: 10px 0 20px 0;
        color: #333;
      }
      header {
        width: 640px;
        margin: auto;
      }
      section {
        width: 640px;
        margin: auto;
      }
      section p {
        margin-bottom: 27px;
        font-size: 20px;
        line-height: 1.6;
        color: #333;
      }
      section img {
        max-width: 640px;
      }
      footer {
        padding: 0 20px;
        margin: 50px 0;
        text-align: center;
        font-size: 12px;
      }
      .aspectRatioPlaceholder {
        max-width: auto !important;
        max-height: auto !important;
      }
      .aspectRatioPlaceholder-fill {
        padding-bottom: 0 !important;
      }
      header,
      section[data-field=subtitle],
      section[data-field=description] {
        display: none;
      }
      </style></head><body><article class="h-entry">
<header>
<h1 class="p-name">Design Patterns to Follow in Kotlin: A Guide to Better Code</h1>
</header>
<section data-field="subtitle" class="p-summary">
Kotlin is a modern, statically typed programming language that was designed to improve upon Java. It has a clean syntax, supports…
</section>
<section data-field="body" class="e-content">
<section name="e571" class="section section--body section--first section--last"><div class="section-divider"><hr class="section-divider"></div><div class="section-content"><div class="section-inner sectionLayout--insetColumn"><h3 name="d5a2" id="d5a2" class="graf graf--h3 graf--leading graf--title">Design Patterns to Follow in Kotlin: A Guide to Better Code</h3><figure name="43a6" id="43a6" class="graf graf--figure graf-after--h3"><img class="graf-image" data-image-id="1*Kt6Mj-XtM-0IxygY_5iJ_A.png" data-width="649" data-height="390" data-is-featured="true" alt="Kotlin Builder Pattern" src="https://cdn-images-1.medium.com/max/800/1*Kt6Mj-XtM-0IxygY_5iJ_A.png"><figcaption class="imageCaption">Builder Pattern in Kotlin</figcaption></figure><p name="60d8" id="60d8" class="graf graf--p graf-after--figure">Kotlin is a modern, statically typed programming language that was designed to improve upon Java. It has a clean syntax, supports functional programming, and provides many features that make it easier to write high-quality, maintainable code. In this blog, we will explore some of the most important design patterns that should be followed in Kotlin to write better code.</p><h3 name="6bb8" id="6bb8" class="graf graf--h3 graf-after--p"><strong class="markup--strong markup--h3-strong">Null Safety</strong></h3><p name="7601" id="7601" class="graf graf--p graf-after--h3">One of the most significant problems with Java is the prevalence of <code class="markup--code markup--p-code">NullPointerException</code>s. To address this issue, Kotlin introduces null safety, which prevents null references from being assigned to variables by default.</p><pre data-code-block-mode="2" spellcheck="false" data-code-block-lang="kotlin" name="3742" id="3742" class="graf graf--pre graf-after--p graf--preV2"><span class="pre--content"><span class="hljs-keyword">val</span> name: String = <span class="hljs-string">&quot;John Doe&quot;</span><br /><span class="hljs-keyword">val</span> age: <span class="hljs-built_in">Int</span> = <span class="hljs-number">25</span></span></pre><p name="3676" id="3676" class="graf graf--p graf-after--pre">In the example above, <code class="markup--code markup--p-code">name</code> and <code class="markup--code markup--p-code">age</code> are non-nullable variables. If you try to assign <code class="markup--code markup--p-code">null</code> to them, the compiler will give an error. If you want to allow null values, you can use the <code class="markup--code markup--p-code">?</code> operator.</p><pre data-code-block-mode="2" spellcheck="false" data-code-block-lang="kotlin" name="5121" id="5121" class="graf graf--pre graf-after--p graf--preV2"><span class="pre--content"><span class="hljs-keyword">val</span> name: String? = <span class="hljs-literal">null</span><br /><span class="hljs-keyword">val</span> age: <span class="hljs-built_in">Int</span>? = <span class="hljs-literal">null</span></span></pre><h3 name="defb" id="defb" class="graf graf--h3 graf-after--pre"><strong class="markup--strong markup--h3-strong">Extension Functions</strong></h3><p name="3c1f" id="3c1f" class="graf graf--p graf-after--h3">Kotlin provides the ability to extend a class with additional functions without having to inherit from it. This is achieved through extension functions.</p><pre data-code-block-mode="2" spellcheck="false" data-code-block-lang="kotlin" name="6221" id="6221" class="graf graf--pre graf-after--p graf--preV2"><span class="pre--content"><span class="hljs-function"><span class="hljs-keyword">fun</span> String.<span class="hljs-title">upperCaseFirstLetter</span><span class="hljs-params">()</span></span> : String {<br />    <span class="hljs-keyword">return</span> <span class="hljs-keyword">this</span>.substring(<span class="hljs-number">0</span>, <span class="hljs-number">1</span>).toUpperCase() + <span class="hljs-keyword">this</span>.substring(<span class="hljs-number">1</span>)<br />}<br /><br /><span class="hljs-comment">// Usage:</span><br />println(<span class="hljs-string">&quot;hello&quot;</span>.upperCaseFirstLetter()) <span class="hljs-comment">// Hello</span></span></pre><h3 name="820d" id="820d" class="graf graf--h3 graf-after--pre"><strong class="markup--strong markup--h3-strong">Singleton</strong></h3><p name="f44d" id="f44d" class="graf graf--p graf-after--h3">A singleton is a design pattern that restricts a class to have only one instance and provides a global point of access to it. In Kotlin, this can be achieved using the <code class="markup--code markup--p-code">object</code> keyword.</p><pre data-code-block-mode="2" spellcheck="false" data-code-block-lang="kotlin" name="8fa3" id="8fa3" class="graf graf--pre graf-after--p graf--preV2"><span class="pre--content"><span class="hljs-keyword">object</span> Singleton {<br />    <span class="hljs-keyword">val</span> name = <span class="hljs-string">&quot;Singleton&quot;</span><br />    <span class="hljs-function"><span class="hljs-keyword">fun</span> <span class="hljs-title">printName</span><span class="hljs-params">()</span></span> {<br />        println(name)<br />    }<br />}<br /><br /><span class="hljs-comment">// Usage:</span><br />Singleton.printName() <span class="hljs-comment">// Singleton</span></span></pre><h3 name="40b9" id="40b9" class="graf graf--h3 graf-after--pre"><strong class="markup--strong markup--h3-strong">Builder</strong></h3><p name="7c14" id="7c14" class="graf graf--p graf-after--h3">The builder pattern is a creational design pattern that allows for a flexible way to construct complex objects. In Kotlin, the builder pattern can be achieved through the use of secondary constructors and default values.</p><pre data-code-block-mode="2" spellcheck="false" data-code-block-lang="kotlin" name="c9f2" id="c9f2" class="graf graf--pre graf-after--p graf--preV2"><span class="pre--content"><span class="hljs-keyword">data</span> <span class="hljs-keyword">class</span> <span class="hljs-title class_">User</span>(<span class="hljs-keyword">val</span> name: String, <span class="hljs-keyword">val</span> age: <span class="hljs-built_in">Int</span>, <span class="hljs-keyword">val</span> address: String = <span class="hljs-string">&quot;&quot;</span>)<br /><br /><span class="hljs-keyword">class</span> <span class="hljs-title class_">UserBuilder</span> {<br />    <span class="hljs-keyword">var</span> name = <span class="hljs-string">&quot;&quot;</span><br />    <span class="hljs-keyword">var</span> age = <span class="hljs-number">0</span><br />    <span class="hljs-keyword">var</span> address = <span class="hljs-string">&quot;&quot;</span><br /><br />    <span class="hljs-function"><span class="hljs-keyword">fun</span> <span class="hljs-title">build</span><span class="hljs-params">()</span></span> = User(name, age, address)<br />}<br /><br /><span class="hljs-comment">// Usage:</span><br /><span class="hljs-keyword">val</span> user = UserBuilder().apply {<br />    name = <span class="hljs-string">&quot;John Doe&quot;</span><br />    age = <span class="hljs-number">25</span><br />}.build()</span></pre><p name="e477" id="e477" class="graf graf--p graf-after--pre">In conclusion, these design patterns are just a few of the many techniques that can be used to write better code in Kotlin. By embracing these patterns and following best practices, you can write code that is more concise, readable, and maintainable.</p><p name="2f71" id="2f71" class="graf graf--p graf-after--p graf--trailing">Happy Coding!!</p></div></div></section>
</section>
<footer><p>By <a href="https://medium.com/@investfy" class="p-author h-card">⎈ INVĘSƮƒ¥ | | ENĞINEÊR ™</a> on <a href="https://medium.com/p/a81649aa8ec7"><time class="dt-published" datetime="2023-02-05T14:31:37.290Z">February 5, 2023</time></a>.</p><p><a href="https://medium.com/@investfy/design-patterns-to-follow-in-kotlin-a-guide-to-better-code-a81649aa8ec7" class="p-canonical">Canonical link</a></p><p>Exported from <a href="https://medium.com">Medium</a> on August 21, 2025.</p></footer></article></body></html>
