# Jekyll

[Instalacja](https://github.com/mojombo/jekyll/wiki/install) gemów
*jekyll* i *rdiscount*:
```sh
gem install jekyll
gem install rdiscount
```

Instalacja programu do kolorwania kodu [Pygments](http://pygments.org/):
```sh
sudo easy_install Pygments         # as root
sudo easy_install --user Pygments  # in user site-package
pygmentize -V                      # v1.6, dodać do PATH
pygmentize -S default -f html > pygments.css
```

## Użycie

[Jak działa Jekyll](https://github.com/mojombo/jekyll/wiki/usage):
```
.
|-- _config.yml
|-- images/
|-- css
|   `-- blog.css
|-- _layouts
|   |-- default.html
|   |-- index.html
|   `-- post.html
|-- _posts
|   |-- 2013-02-29-why-every-programmer-likes-jekyll.md
|   `-- 2013-01-01-postanowienia-na-nowy-rok.md
|-- _site
`-- index.html
```

Konfiguracja konwertera z notacji Markdown na HTML
oraz kolorowanie składni, *_config.yml:
```yaml
markdown: rdiscount
pygments: true
permalink: ":year/:month/:day/:title/"
```
Dopisujemy do szablonów:
```html
<link href="../../../../pygments.css" rel="stylesheet">
```

Każdy post zaczynamy od tzw. *front matter*, np:

---
layout: post
title: Jekyll-Blog HOWTO
tags: [jekyll, example]
description: "przykładowy post"
---
