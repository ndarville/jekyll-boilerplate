Jekyll Project Boilerplate
==========================
[![Build Status](https://travis-ci.org/ndarville/jekyll-boilerplate.svg?branch=master)](https://travis-ci.org/ndarville/jekyll-boilerplate?branch=master)
[![MIT-license badge](http://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/ndarville/jekyll-boilerplate/blob/master/LICENSE.md)
[![Dependency Status](https://gemnasium.com/ndarville/jekyll-boilerplate.svg?branch=master)](https://gemnasium.com/ndarville/jekyll-boilerplate)

A template for building a static website with the Ruby CMS [Jekyll][jekyll], as well as a project-directory template for how I, **@ndarville**, aim to start on each project.

## Local Installation
Assuming Ruby and Git are installed:

1. `git clone git@github.com:ndarville/jekyll-boilerplate.git`
2. `cd jekyll-boilerplate`
3. `bundle install`
4. `bundle exec jekyll serve --watch`

This creates a `_site/` folder and starts a `localhost:4000` server.

## Deployment

### On GitHub.io
1. Create a GitHub repo with the name `githubusername.github.io`.
2. Clone the boilerplate with `git clone git@github.com:ndarville/jekyll-boilerplate.git`.
3. `cd jekyll-boilerplate`.
4. Delete both `.lock` files.
5. Delete `Gemfile.github-pages`; you won't be needing this.
6. `bundle install`.
7. Push your new site to `githubusername.github.io`.
8. Done! For more, see [the official GitHub Pages site][gp].

For an example project, visit [my GitHub site][ndarville.io].

#### Using a Custom Domain
1. Create a `CNAME` file in root with the line `githubusername.github.io`.
2. Configure DNS using [this][custom-guide] guide by GitHub.

For an example of a GitHub-hosted site with a custom domain, see [my Hafnia Times project][hafnia].

### On AWS
1. Clone the boilerplate with `git clone git@github.com:ndarville/jekyll-boilerplate.git`.
2. `cd jekyll-boilerplate`.
3. Delete both `.lock` files.
4. Delete `Gemfile` and rename `Gemfile.github-pages` to `Gemfile`.
5. `bundle install`
6. Build your site with `bundle exec jekyll build`.
7. Rename `_s3_website.yml` by removing the prepended underscore.
8. Enter your AWS credentials in `s3_website.yml`.
9. `s3_website cfg apply` will configure AWS.
10. You can say `[y]es` to setting up CloudFront, if you want. You can just type `[n]o` for now.
11. Push your built site to AWS with `s3_website push`.

    `s3_website` automatically recognizes the folder `_site` and deploys it. If you want to push a folder with a different name, use `s3_website push --site="yourfoldername"`.
12. Done!

From now on, just use `s3_website push` to deploy your changes. For more info on using `s3_website`, consult [its docs][s3].

## Asides
Page files are in [Markdown][markdown], .markdown. They are viewable in any text editor, but try out [Mou][mou] if you want to see the rendered version.

As usual, you can update your `style.css` with the changes to `style.scss` by running `sass --watch style.scss:style.css` in `static/css/`.

Leave feedback and questions in Issues, if you want.

## Testing and Travis CI
The boilerplate comes with its own [Travis CI configuration][travis]. It would be silly not to use it. See what it does for this repo over [here][travis-example].

## “Your `s3_website` Gem Is Out of Date, Dudeski”
I know. The reason is that [versions from `2.0` require Java][s3-java], and I know I personally don’t want anything to do with Java, if I can help it.

## License
MIT License.


[jekyll]: http://jekyllrb.com
[gp]: https://pages.github.com
[ndarville.io]: https://github.com/ndarville/ndarville.github.io
[hafnia]: https://github.com/hafniatimes/hafniatimes.github.io
[custom-guide]: https://help.github.com/articles/setting-up-a-custom-domain-with-github-pages
[s3]: https://github.com/laurilehmijoki/s3_website
[markdown]: http://daringfireball.net/projects/markdown/
[mou]: http://mouapp.com/
[travis]: https://github.com/ndarville/jekyll-boilerplate/blob/master/.travis.yml
[travis-example]: https://travis-ci.org/ndarville/jekyll-boilerplate/
[s3-java]: https://github.com/laurilehmijoki/s3_website/blob/master/changelog.md#200
