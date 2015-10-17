---
layout: page
title: About
---

# Web-version of Master's Thesis
Publishing the thesis for my dual Master's at MIT in Tranportation and City Planning in a  more accesible format while testing some web programming. I'm using [jekyll](http://jekyllrb.com) on a machine running `Ubuntu 14.04` for this project. This is **work in progress**, which you can see [here](https://radumas.github.io/thesis). Until the libraries host the pdf, you can find that [here](https://radumas.github.io/thesis/raw_thesis/Thesis Final.pdf) (16MB pdf). 

## Workflow  

### 1.  Install Jekyll
I used a modified version of [these instructions](https://help.github.com/articles/using-jekyll-with-pages/). 
1. In `Ubuntu 14.04` this required installing `ruby 2.2.2` using the [gorails guide](https://gorails.com/setup/ubuntu/14.04) and the `rbenv` method. First installing dependencies
{% highlight bash %}
sudo apt-get install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev python-software-properties libffi-dev
{% endhighlight %}
2. then running
{% highlight bash %}
cd
git clone git://github.com/sstephenson/rbenv.git .rbenv
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc
echo 'eval "$(rbenv init -)"' >> ~/.bashrc
exec $SHELL

git clone git://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build
echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc
exec $SHELL

git clone https://github.com/sstephenson/rbenv-gem-rehash.git ~/.rbenv/plugins/rbenv-gem-rehash

rbenv install 2.2.2
rbenv global 2.2.2
ruby -v
{% endhighlight %}

3. Then "telling Rubygems not to install the documentation for each package locally and then install Bundler"
{% highlight bash %}
echo "gem: --no-ri --no-rdoc" > ~/.gemrc
sudo gem install bundler
{% endhighlight %}
4.  _Optional Ubuntu step_ `nodejs` is [required](http://stackoverflow.com/a/9333316/4047679) install it, and then [fix](http://askubuntu.com/questions/477577/alias-of-nodejs-as-node-on-14-04?lq=1) the problem with the `nodejs` being run under the `nodejs` command when most node-related things expect `node`.
{% highlight bash %}
sudo apt-get install nodejs
sudo ln -s /usr/local/bin/nodejs /usr/bin/node
{% endhighlight %}

5.  In the project directory typing `bundle init` and then editing the newly created `Gemfile` to contain
{% highlight bash %}
source 'https://rubygems.org'
gem 'github-pages'
{% endhighlight %}

6. then installing with `bundle install`
     
### 2.  Convert thesis from *docx* to *markdown* using pandoc. 
This extracts images from the thesis to a [folder](https://github.com/jgm/pandoc/issues/1986). Chapter titles were not rendered with the header markdown, but these will become individual posts so it didn't matter. Not all images were extracted, since some were excel graphs that weren't images. The `mathjax` flag should convert equations to MathJax for display
{% highlight bash %}
pandoc -f docx -t markdown_github -o index.md --mathjax --extract-media=images Thesis.docx
{% endhighlight %}
Most headers had to be manually modified since, I think, Word also thought of them as lists. Pandoc converted a number of headers with `<span>` and `<anchor>` tags, I think with a table of contents in mind. So these were manually removed, and the headings properly formatted. MathJax equations had to be surrounded by `<div>` or `<span>` [tags](http://stackoverflow.com/questions/10987992/using-mathjax-with-jekyll).

### 3.  Build site with 
{% highlight bash %}
bundle exec jekyll build
{% endhighlight %}

### 4.  Commit to github 
{% highlight bash %}
git add --all
git commit -m "MESSAGE"
git push origin gh-pages
{% endhighlight %}

### 5. Choose a Template
While the Code for America Annual Report is a beautiful webpage, it doesn't really follow the principles of Jekyll terribly closely, i.e., most sections are individually styled, which leads to more editing of SASS than I would've wanted, so I'm switched to the [Notepad theme](https://github.com/hmfaysal/Notepad/).

Can add `reversed` to the liquid loops `for p in site.posts reversed` to display posts in order to display them in chronological order of their filenames, which makes working with the files less of a hassle.


## TODO
- [x] Split Chapters into posts
- [ ] Add MBTA & NSERC logos to acknowledgements
- [ ] Link to about page
- [ ] Find missing images
- [ ] Equation 42 temporarily deleted so jekyll will build properly. Need to fix MathJax notation
- [ ] Make the thing lay-person readable
- [ ] Add links to other theses
- [ ] Format citations somehow
- [ ] Footnotes are at the end
