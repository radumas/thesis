# Web-version of Master's Thesis
Publishing the thesis for my dual Master's at MIT in Tranportation and City Planning in a  more accesible format while testing some web programming. I'm using [jekyll](http://jekyllrb.com) on a machine running `Ubuntu 14.04` for this project.

## Workflow
1. [Install Jekyll](https://help.github.com/articles/using-jekyll-with-pages/). In `Ubuntu 14.04` this required installing `ruby 2.2.2` using the [gorails guide](https://gorails.com/setup/ubuntu/14.04) and the `rbenv` method. First installing dependencies

        sudo apt-get install git-core curl zlib1g-dev build-essential libssl-dev libreadline-dev libyaml-dev libsqlite3-dev sqlite3 libxml2-dev libxslt1-dev libcurl4-openssl-dev python-software-properties libffi-dev

  then running

```
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
```

  then "telling Rubygems not to install the documentation for each package locally and then install Bundler"

        echo "gem: --no-ri --no-rdoc" > ~/.gemrc
        sudo gem install bundler

  In the project directory typing `bundle init` and then editing the newly created `Gemfile` to contain

        source 'https://rubygems.org'
        gem 'github-pages'

  then installing with `bundle install`
     
2.  Convert thesis from `docx` to `markdown` using pandoc. This extracts images from the thesis to a folder. Links must be modified to be relative. Chapter titles were not rendered with the header markdown, but these will become individual posts so it didn't matter.

        pandoc -f docx -t markdown_github -o ~/thesis/_posts/thesis.md --extract-media=~/thesis/images Thesis.docx
        
