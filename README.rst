=======================
github pages and Jekyll
=======================

Overview
--------

github Pages可以被认为是用户编写的、托管在github上的静态网页。
github提供模板，允许站内生成网页，但也允许用户自己编写网页，然后上传。有意思的是，这种上传并不是单纯的上传，而是会经过Jekyll程序的再处理。

Jekyll（发音/'dʒiːk əl/，"杰克尔"）是一个静态站点生成器，它会根据网页源码生成静态文件。它提供了模板、变量、插件等功能，所以实际上可以用来编写整个网站。

::

    on github, create the new repository 'github-pages'

    $ mkdir github-pages
    $ cd github-pages
    $ git init
    $ echo 'hello' > readme
    $ git add .
    $ git ci -m 'init repo'
    $ git remote add origin https://github.com/username/github-pages.git
    $ git push origin master

    $ git checkout --orphan gh-pages
    $ git rm -rf .

    // edit the _config.yml, _layouts, _posts and index.html

    $ git add .
    $ git ci -m 'first pages commit'
    $ git push origin gh-pages



    
