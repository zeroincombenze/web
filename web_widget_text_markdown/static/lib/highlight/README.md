[![Build Status](https://travis-ci.org/zeroincombenze/highlight.svg?branch=10.0)](https://travis-ci.org/zeroincombenze/highlight)
[![license agpl](https://img.shields.io/badge/licence-AGPL--3-blue.svg)](http://www.gnu.org/licenses/agpl-3.0.html)
[![Coverage Status](https://coveralls.io/repos/github/zeroincombenze/highlight/badge.svg?branch=10.0)](https://coveralls.io/github/zeroincombenze/highlight?branch=10.0)
[![codecov](https://codecov.io/gh/zeroincombenze/highlight/branch/10.0/graph/badge.svg)](https://codecov.io/gh/zeroincombenze/highlight/branch/10.0)
[![OCA_project](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-oca-10.svg)](https://github.com/OCA/highlight/tree/10.0)
[![Tech Doc](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-docs-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/dev)
[![Help](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-help-10.svg)](http://wiki.zeroincombenze.org/en/Odoo/10.0/man/)
[![try it](http://www.zeroincombenze.it/wp-content/uploads/ci-ct/prd/button-try-it-10.svg)](http://erp10.zeroincombenze.it)


[![en](https://github.com/zeroincombenze/grymb/blob/master/flags/en_US.png)](https://www.facebook.com/groups/openerp.italia/)

# Highlight.js
==============


Highlight.js is a syntax highlighter written in JavaScript. It works in the
browser as well as on the server. It works with pretty much any markup,
doesn't depend on any framework and has automatic language detection.


## Getting Started

The bare minimum for using highlight.js on a web page is linking to the library
along with one of the styles and calling [`initHighlightingOnLoad`][1]:

```html
<link rel="stylesheet" href="/path/to/styles/default.css">
<script src="/path/to/highlight.pack.js"></script>
<script>hljs.initHighlightingOnLoad();</script>
```

This will find and highlight code inside of `<pre><code>` tags trying to detect
the language automatically. If automatic detection doesn't work for you, you can
specify the language in the class attribute:

```html
<pre><code class="html">...</code></pre>
```

The list of supported language classes is available in the [class reference][8].
Classes can also be prefixed with either `language-` or `lang-`.

To disable highlighting altogether use the `nohighlight` class:

```html
<pre><code class="nohighlight">...</code></pre>
```

## Custom Initialization

When you need a bit more control over the initialization of
highlight.js, you can use the [`highlightBlock`][2] and [`configure`][3]
functions. This allows you to control *what* to highlight and *when*.

Here's an equivalent way to calling [`initHighlightingOnLoad`][1] using jQuery:

```javascript
$(document).ready(function() {
  $('pre code').each(function(i, block) {
    hljs.highlightBlock(block);
  });
});
```

You can use any tags instead of `<pre><code>` to mark up your code. If you don't
use a container that preserve line breaks you will need to configure
highlight.js to use the `<br>` tag:

```javascript
hljs.configure({useBR: true});

$('div.code').each(function(i, block) {
  hljs.highlightBlock(block);
});
```

For other options refer to the documentation for [`configure`][3].


## Getting the Library

You can get highlight.js as a hosted or custom-build browser script or as a
server module. Head over to the [download page][4] for all the options.

Note, that the library is not supposed to work straight from the source on
GitHub, it requires building. If none of the pre-packaged options work for you
refer to the [building documentation][5].


## License

Highlight.js is released under the BSD License. See [LICENSE][10] file for
details.


## Links

The official site for the library is at <https://highlightjs.org/>.

Further in-depth documentation for the API and other topics is at
<http://highlightjs.readthedocs.org/>.

Authors and contributors are listed in the [AUTHORS.en.txt][9] file.

[1]: http://highlightjs.readthedocs.org/en/latest/api.html#inithighlightingonload
[2]: http://highlightjs.readthedocs.org/en/latest/api.html#highlightblock-block
[3]: http://highlightjs.readthedocs.org/en/latest/api.html#configure-options
[4]: https://highlightjs.org/download/
[5]: http://highlightjs.readthedocs.org/en/latest/building-testing.html
[8]: http://highlightjs.readthedocs.org/en/latest/css-classes-reference.html
[9]: https://github.com/isagalaev/highlight.js/blob/master/AUTHORS.en.txt
[10]: https://github.com/isagalaev/highlight.js/blob/master/LICENSE

[//]: # (copyright)

----

**Odoo** is a trademark of [Odoo S.A.](https://www.odoo.com/) (formerly OpenERP, formerly TinyERP)

**OCA**, or the [Odoo Community Association](http://odoo-community.org/), is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

**zeroincombenze®** is a trademark of [SHS-AV s.r.l.](http://www.shs-av.com/)
which distributes and promotes **Odoo** ready-to-use on its own cloud infrastructure.
[Zeroincombenze® distribution](http://wiki.zeroincombenze.org/en/Odoo)
is mainly designed for Italian law and markeplace.
Everytime, every Odoo DB and customized code can be deployed on local server too.

[//]: # (end copyright)

[//]: # (addons)

[//]: # (end addons)

[![chat with us](https://www.shs-av.com/wp-content/chat_with_us.gif)](https://tawk.to/85d4f6e06e68dd4e358797643fe5ee67540e408b)
