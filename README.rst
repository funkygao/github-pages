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
    $ git remote add origin https://github.com/funkygao/github-pages.git
    $ git push origin master

    $ git checkout --orphan gh-pages
    $ git rm -rf .

    // edit the _config.yml, _layouts, _posts and index.html

    $ git add .
    $ git ci -m 'first pages commit'
    $ git push origin gh-pages


    http://funkygao.github.com/github-pages/

   
DNS
---
如果不想用http://funkygao.github.com/github-pages/这个域名，可以换成自己的域名。

具体方法是在repo的根目录下面，新建一个名为CNAME的文本文件，里面写入你要绑定的域名，比如example.com或者xxx.example.com。

如果绑定的是顶级域名，则DNS要新建一条A记录，指向204.232.175.78。
如果绑定的是二级域名，则DNS要新建一条CNAME记录，指向funkygao.github.com。

此外，别忘了将_config.yml文件中的baseurl改成根目录"/"。

