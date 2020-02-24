---
layout: post
categories: jekyll cheatsheet
author: Naman Attri
---
Jekyll is a static site generator. We can use simple markdown to create static web pages without using any backend database.

## Installation

Install ruby on the OS of your liking. Below are the instructions for ubuntu:
```bash
sudo apt-get install ruby-full build-essential zlib1g-dev

echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

# install jekyll & bundler
gem install jekyll
gem install bundler
```

## Create project
CD into the directory you prefer:
```bash
jekyll new proj1

cd proj1

bundle exec jekyll serve
```
Site will be running on <a href="http://localhost:4000" target="_blank">http://localhost:4000</a>

## Gems
Gems are to ruby what packages are to nodejs.
```bash
gem install bundler
gem install a0-tzmigration-ruby
```

## Gemfile
Gemfile contains list of gems that our site is dependent on. Gemfile is to ruby what package.json is to nodejs.
```rb
source "https://rubygems.org"

gem "jekyll"

group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-seo-tag"
end
```

## Bundler
Bundler installs the gems that are listed in the Gemfile. Used to lock dependency versions across different instances of the same project running in different environments.
```bash
# when using Gemfile
cd proj1
bundle install
bundle exec jekyll serve

# when not using Gemfile
jekyll serve
```

Source: <a href="https://jekyllrb.com/docs/" target="_blank">jekyll</a>