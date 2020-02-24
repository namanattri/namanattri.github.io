---
layout: post
categories: jekyll cheatsheet
author: Naman Attri
---
Source: <a href="https://jekyllrb.com/docs/" target="_blank">jekyll</a>

# What is jekyll?
Jekyll is a static site generator. We can use simple markdown to create static web pages without using any backend database.

# Installation

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

# Create project
CD into the directory you prefer:
```bash
jekyll new proj1

cd proj1

bundle exec jekyll serve
```
Site will be running on <a href="http://localhost:4000" target="_blank">http://localhost:4000</a>