---
layout: post
title: "MathJax"
date: 2012-02-02 23:45
comments: true
categories: [mathjax, tex, math notation]
---

1\. Dopisujemy do *source/_includes/custom/head.html*:

```html source/_includes/custom/head.html
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
  extensions: ["jsMath2jax.js"],
  tex2jax: {
    inlineMath: [ ['$', '$'], ['\\(', '\\)'] ],
    displayMath: [ ['$$', '$$'], ["\\[", "\\]"] ],
    processEscapes: true
  },

  "HTML-CSS": { scale: 105 },

  displayAlign: "left",
  displayIndent: "2em",

  styles: {
    ".MathJax_Display": { "color": "#A00" },
    ".MathJax": { "color": "#A00" }
  }
});
</script>
<script src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS_HTML"></script>
```

Zobacz też [Configuration Objects](http://www.mathjax.org/docs/1.1/options/index.html).


2\. Wzory wystawione wpisujemy tak:

```html
<div class=math>
\int\! f(x)\,dx \lt \infty
</div>
```

Oto rezultat:

<div class=math>
\int\! f(x)\,dx \lt \infty
</div>

3\. Wzory w akapicie wpisujemy tak:

```html
Euler formula: $e^{i\pi} + 1 = 0$.
```

Oto rezultat:

<p>Euler formula: $e^{i\pi} + 1 = 0$.</p>


4\. Nie każde polecenia LaTeX-a jest poprawnie renderowane przez MathJax.
 Lista poleceń poprawnie interpretowanych jest tutaj:
[Supported LaTeX commands](http://www.mathjax.org/docs/1.1/tex.html#supported-latex-commands).


## Web Equation

Co to jest? Wchodzimy na stronę
[Web Equation](http://webdemo.visionobjects.com/equation.html?locale=default)
i wszystko jasne!

