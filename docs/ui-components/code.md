---
layout: default
title: Code
parent: Markdown Help
has_children: true
nav_order: 7
---

# Code
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Inline code

Code can be rendered inline by wrapping it in single back ticks.

<div class="code-example" markdown="1">
Lorem ipsum dolor sit amet, `<inline code snippet>` adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

## Heading with `<inline code snippet>` in it.
{: .no_toc }
</div>
```markdown
Lorem ipsum dolor sit amet, `<inline code snippet>` adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.

## Heading with `<inline code snippet>` in it.
```

---

## Syntax highlighted code blocks

Use Jekyll's built-in syntax highlighting with Rouge for code blocks by using three backticks, followed by the language name:

<div class="code-example" markdown="1">
```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```
</div>
{% highlight markdown %}
```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```
{% endhighlight %}

---

## Code blocks with rendered examples

To demonstrate front end code, sometimes it's useful to show a rendered example of that code. After including the styles from your project that you'll need to show the rendering, you can use a `<div>` with the `code-example` class, followed by the code block syntax. If you want to render your output with Markdown instead of HTML, use the `markdown="1"` attribute to tell Jekyll that the code you are rendering will be in Markdown format... This is about to get meta...

<div class="code-example" markdown="1">

<div class="code-example" markdown="1">

[Link button](https://just-the-docs.com){: .btn }

</div>
```markdown
[Link button](https://just-the-docs.com){: .btn }
```

</div>
{% highlight markdown %}
<div class="code-example" markdown="1">

[Link button](https://just-the-docs.com){: .btn }

</div>
```markdown
[Link button](https://just-the-docs.com){: .btn }
```
{% endhighlight %}

---



## Copy button
{: .d-inline-block }

New (v0.4.0)
{: .label .label-green }

The copy button for code blocks can be enabled or disabled via the `enable_copy_code_button` key in `_config.yml`. By default, the value of this key is `false`; users need to opt-in.

```yaml
# For copy button on code
enable_copy_code_button: true
```

Note that this feature requires JavaScript; if JavaScript is disabled in the browser, this feature will not work. In addition, this feature uses `navigator.clipboard`, which is only available in [secure contexts](https://developer.mozilla.org/en-US/docs/Web/Security/Secure_Contexts) (such as over HTTPS). If the site is viewed in an insecure context, the copy button will not work ([relevant issue: #1202](https://github.com/just-the-docs/just-the-docs/issues/1202)).

The content on this page is under an [MIT License](https://github.com/just-the-docs/just-the-docs/blob/main/LICENSE.txt).