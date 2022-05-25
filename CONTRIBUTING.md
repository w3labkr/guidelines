# Contributing Guide

[Jekyll](https://jekyllrb.com/) is a static site generator. It takes text written in your favorite markup language and uses layouts to create a static website.

## Quickstart

Install the jekyll and bundler gems:

```shell
gem install bundler jekyll
```

To install gems in your Gemfile using Bundler, run the following in the directory that has the Gemfile:

```shell
bundle install
bundle exec jekyll serve
```

Pass the --livereload option to serve to automatically refresh the page with each change you make to the source files:

```shell
bundle exec jekyll serve --livereload
```

## Troubleshooting

You have already activated i18n 1.10.0, but your Gemfile requires i18n 0.9.5. Prepending `bundle exec` to your command may solve this.

```shell
$ ruby -S gem list --local | grep i18n
i18n (1.10.0, 0.9.5)

$ bundle exec jekyll serve
```

If you are using Ruby version 3.0.0 or higher, step 5 may fail. You may fix it by adding webrick to your dependencies:

```shell
bundle add webrick
bundle exec jekyll serve
```

[You have already activated i18n 1.8.11, but your Gemfile requires i18n 0.9.5. Prepending bundle exec to your command may solve this. (Gem::LoadError)](https://github.com/Homebrew/brew.sh/issues/845)
