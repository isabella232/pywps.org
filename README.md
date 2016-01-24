
[![Build Status](https://travis-ci.org/geopython/pywps.org.png)](https://travis-ci.org/geopython/pywps.org)

# pywps.org

This is the setup for http://pywps.org

## Setting up website environment locally

```bash
# setup virtualenv
virtualenv pywps.org && cd $_
. bin/activate
# get the repo
git clone git@github.com:geopython/pywps.org.git && cd pywps.org
# set Ruby environment variables
. setenv-ruby-gem
# install Jekyll
gem install jekyll link-checker jekyll-mentions jekyll-sitemap github-pages
```

## Workflow

```bash
# edit / verify content
jekyll build
jekyll serve  # default port is 4000, set explicitly with -P 
# commit and push
git commit -m 'update website'
git push origin gh-pages
# check links
check-links _site
# view at http://localhost:4000
# adding blogposts
cd _drafts
vi newpost.md
# make sure to set the following YAML front matter:
# layout: post
# title: Some Title
# author: Firstname Lastname
# author_url: URL to link to the author (Twitter, GitHub, etc.)
# preview with `make drafts` and draft will show up as latest post
# when you are ready to publish:
# - rename the file as per the current YYYY-MM-DD
git mv _drafts/newpost.md _posts/YYYY-MM-DD-newpost.md
vi _posts/YYYY-MM-DD-newpost.md
# update the publish_date YAML front matter
# commit and push
git commit -m 'publish article'
git push origin gh-pages
```

For a [Sphinx](http://sphinx-doc.org/) feel, there's a `Makefile` with
the familiar targets:

```bash
make html
make linkcheck
make clean
make drafts
```

## Minimal Theme

pywps.org uses the [Minimal Theme](http://orderedlist.github.com/minimal) from [GitHub Pages](http://pages.github.com/).

Syntax highlighting is provided on GitHub Pages by [Pygments](http://pygments.org).
