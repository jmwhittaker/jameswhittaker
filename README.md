JamesWhittaker.com
==================

This is the source of my personal website and blog [jameswhittaker.com](http://jameswhittaker.com).

It utilises the static site generator Jekyll to generate the required static HTML and CSS.

Hosted by Github pages as project pages.

Branches
--------

There are two branches in this repo **'master'** and **'gh-pages'**. The Jekyll source files are held within the master branch. **gh-pages** branch has the built HTML output from the master branch.

Main reason is you can't have any custom Jekyll plugins when you want your pages to be built from Github automatically.

Having this two branch approach get's around this issue by only servbing up the generated static HTML. Simples.

Getting started
---------------

* Install Jekyll
* Checkout the repo
* Start the Jekyll server and watch for file changes `jekyll --server --auto`
* Open your browser to <http://localhost:4000>
