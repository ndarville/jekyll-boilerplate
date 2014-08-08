Jekyll Project Boilerplate
==========================
[![Build Status](https://travis-ci.org/ndarville/jekyll-boilerplate.svg?branch=master)](https://travis-ci.org/ndarville/jekyll-boilerplate?branch=master)
[![MIT-license badge](http://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/ndarville/jekyll-boilerplate/blob/master/LICENSE.md)
[![Dependency Status](https://gemnasium.com/ndarville/jekyll-boilerplate.svg?branch=master)](https://gemnasium.com/ndarville/jekyll-boilerplate)

A template for building a static website with the Ruby CMS [Jekyll][jekyll], as well as a project-directory template for how I, @ndarville, aim to start on each project.

## Installation
Assuming Ruby and Git are installed:

1. `git clone git@github.com:ndarville/jekyll-boilerplate.git`
2. `cd jekyll-boilerplate`
3. `bundle install`
4. `bundle exec jekyll serve --watch`

This creates a `_site/` folder and starts a `localhost:4000` server.

## Asides
Page files are in [Markdown][markdown], .markdown. They are viewable in any text editor, but try out [Mou][mou] if you want to see the rendered version.

As usual, you can update your `style.css` with the changes to `style.scss` by running `sass --watch style.scss:style.css` in `static/css/`.

Leave feedback and questions in Issues, if you want.

## License
MIT License.


[jekyll]: http://jekyllrb.com
[markdown]: http://daringfireball.net/projects/markdown/
[mou]: http://mouapp.com/
