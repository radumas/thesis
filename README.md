#Analyzing Transit Equity Using Automatically Collected Data
##Abstract
By inferring individual passengers’ origins, destinations, and transfers using automatically
collected transit data, transit providers can obtain and analyze larger volumes of information,
with more accuracy, and at more frequent intervals than are available through traditional origin-
destination (OD) surveys. Automatic OD inference can be an input into the analysis and
reporting of agencies’ social goals, such as the provision of equitable service regardless of race,
national origin, or ethnicity, which is federally required in the USA by Title VI of the Civil
Rights Act of 1964. The methodology prescribed in the Title VI regulation, however, has not
adapted to the opportunity to supplement supply metrics with passenger-centric demand metrics
through the availability of OD data. The goal of this thesis is to demonstrate a preliminary
methodology to link automatically inferred OD information from regular transit users to the
demographic data of public transit commuters from the US Census’s American Community
Survey, and to examine variation in passenger-centric metrics such as journey time and speed.  

This study infers origins and destinations in the context of the Massachusetts Bay Transportation
Authority (MBTA). From a sample month of these data, an example of a passenger-centric
analysis is performed by comparing travel times and speeds of trips with origins in areas home to
predominantly Black or African American transit commuters to travel times and speeds of trips
with origins in areas home to predominantly White transit commuters. Commuters from
predominantly Black or African American census tracts are found to have longer travel times and
slower speeds relative to commuters from tracts where commuters are predominantly White.
Differences are within agency specified margins, but are significant, in particular for journeys
involving bus transfers. Short-term solutions such as through-routing of important bus routes and
increasing reliability of bus departures at terminals and long-term solutions such as faster, more
frequent Diesel Multiple Unit rail service are proposed and evaluated to mitigate these
differences.

**Thesis Supervisor: John P. Attanucci**  
_Research Associate of Civil and Environmental Engineering_  
**Thesis Supervisor: Frederick P. Salvucci**  
_Senior Lecturer of Civil and Environmental Engineering_  

# Web-version of Master's Thesis
Publishing the thesis for my dual Master's at MIT in Tranportation and City Planning in a  more accesible format while testing some web programming. I'm using [jekyll](http://jekyllrb.com) on a machine running `Ubuntu 14.04` for this project. This is **work in progress**, which you can see [here](https://radumas.github.io/thesis). Until the libraries host the pdf, you can find that [here](https://radumas.github.io/thesis/raw_thesis/Thesis Final.pdf) (16MB pdf). 

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
```
echo "gem: --no-ri --no-rdoc" > ~/.gemrc
sudo gem install bundler
```
  _Optional Ubuntu step_ `nodejs` is [required](http://stackoverflow.com/a/9333316/4047679) install it, and then [fix](http://askubuntu.com/questions/477577/alias-of-nodejs-as-node-on-14-04?lq=1) the problem with the `nodejs` being run under the `nodejs` command when most node-related things expect `node`.
```
sudo apt-get install nodejs
sudo ln -s /usr/local/bin/nodejs /usr/bin/node
```
  In the project directory typing `bundle init` and then editing the newly created `Gemfile` to contain
```
source 'https://rubygems.org'
gem 'github-pages'
```
  then installing with `bundle install`
     
2.  Convert thesis from `docx` to `markdown` using pandoc. This extracts images from the thesis to a [folder](https://github.com/jgm/pandoc/issues/1986). Chapter titles were not rendered with the header markdown, but these will become individual posts so it didn't matter. Not all images were extracted, since some were excel graphs that weren't images. The `mathjax` flag should convert equations to MathJax for display

        pandoc -f docx -t markdown_github -o index.md --mathjax --extract-media=images Thesis.docx
        
Most headers had to be manually modified since, I think, Word also thought of them as lists. Pandoc converted a number of headers with `<span>` and `<anchor>` tags, I think with a table of contents in mind. So these were manually removed, and the headings properly formatted. MathJax equations had to be surrounded by `<div>` or `<span>` [tags](http://stackoverflow.com/questions/10987992/using-mathjax-with-jekyll).

3.  Build site with `bundle exec jekyll build`

4.  Commit to github 
    ```
    git add --all
    git commit -m "MESSAGE"
    git push origin gh-pages
    ```

5. While the Code for America Annual Report is a beautiful webpage, it doesn't really follow the principles of Jekyll terribly closely, i.e., most sections are individually styled, which leads to more editing of SASS than I would've wanted, so I'm switching to this theme shortly https://github.com/hmfaysal/Notepad/

6. The posts are reverse chronological order
##TODO
- [x] Split Chapters into posts
- [ ] Find missing images
- [ ] Equation 42 temporarily deleted so jekyll will build properly. Need to fix MathJax notation
- [ ] Make the thing lay-person readable
- [ ] Add links to other theses
- [ ] Format citations somehow
- [ ] Footnotes are at the end
