---
layout: page
title: Overview of GitHub Pages
---

The present site is close to the simplest possible. It has a
particular style (using
[Twitter Bootstrap](http://getbootstrap.com)). And my first rule for
minimizing effort is _Modify your desires to match the defaults._

(For example, I don't like how `simple code` is rendered in red within
a gray box. Ultimately I'll try to figure out how to change that, but
for now I just pretend that I like it that way.)

These GitHub Pages sites are constructed by having a `gh-pages` branch
of a GitHub repository, with specific files layed out in a specific
way. To see the structure of such a repository, look at the
[repository for the present site](http://github.com/kbroman/simple_site).

    _includes/
    _layouts/
    _plugins/
    assets/
    pages/
    .gitignore
    License.md
    Rakefile
    ReadMe.md
    _config.yml
    index.md

The directories beginning with an underscore contain materials
defining the basic layout and style for the site. If you
[build the site locally](pages/local_test.html) (for testing
purposes), there will also be a `_site/` directory containing the
actual site (with
[Markdown](https://daringfireball.net/projects/markdown/) files
converted to html). You don't want the `_site/` directory in your
repository, so include that in the `.gitignore` file.

The
[`assets/`](https://github.com/kbroman/simple_site/tree/gh-pages/assets)
directory contains any non-Markdown materials for the site (e.g.,
images or example code). These files won't be touched in the
conversion but will be just copied over as-is.

The
[`pages/`](https://github.com/kbroman/simple_site/tree/gh-pages/pages)
directory contains
[Markdown](https://daringfireball.net/projects/markdown/) files that
will become html pages on your site.

The
[`_config.yml`](https://github.com/kbroman/simple_site/blob/gh-pages/_config.yml)
file contains all sorts of configuration parameters (some of which
you'll need to modify). The [`Rakefile`]() contains instructions for
the conversion; you won't modify this file.

It's best to always include
[`License.md`](https://github.com/kbroman/simple_site/tree/gh-pages/License.md)
and
[`ReadMe.md`](https://github.com/kbroman/simple_site/tree/gh-pages/ReadMe.md)
files. But you wouldn't need these to be placed on the website; they'd
just be viewed in the repository on [GitHub](http://github.com). The
[`_config.yml`](https://github.com/kbroman/simple_site/tree/gh-pages/_config.yml)
file contains
[a line sort of like the following](https://github.com/kbroman/simple_site/blob/gh-pages/_config.yml#L5)
(but listing a few more files), indicating files to _not_ move to the
final site.

    exclude: ["ReadMe.md", "Rakefile", "License.md"]

Finally,
[`index.md`](https://github.com/kbroman/simple_site/blob/gh-pages/index.md)
is the Markdown version of the main page for your site.

The
[`index.md`](https://github.com/kbroman/simple_site/blob/gh-pages/index.md)
file and the Markdown files in
[`pages/`](https://github.com/kbroman/simple_site/blob/gh-pages/pages)
(e.g.,
[the present page](https://github.com/kbroman/simple_site/blob/gh-pages/pages/overview.md);
click the &ldquo;Raw&rdquo; to view the raw Markdown source)
have a header with a particular form:

    ---
    layout: page
    title: simple site
    tagline: Easy websites with GitHub Pages
    ---

In the conversion of the site from Markdown to html, this bit says
that the current file is to be converted with the &ldquo;page&rdquo;
layout, and gives the title and the (optional) &ldquo;tagline.&rdquo;

The rest is basically plain Markdown, though the present site is
configured to use [Kramdown](http://kramdown.gettalong.org/) as the
Markdown converter (via
[this line in the `_config.yml` file](https://github.com/kbroman/simple_site/blob/gh-pages/_config.yml#L23)).
Read about the [Kramdown syntax](http://kramdown.gettalong.org/syntax.html)
or just look at the
[quick reference](http://kramdown.gettalong.org/quickref.html).

Now go to the page about [how to make an independent web site](independent_site.html).