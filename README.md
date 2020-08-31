Install logs (for record)

1. Set up the repo via https://pages.github.com/
You don't have to add index.html. Jekyll will do that for you.

2. Install Ruby, Gem, Jekyll, Mostly following https://jekyllrb.com/docs/installation/macos/
gem install jekyll -v 3.8.5
# https://pages.github.com/versions/ # version number is from here

3. Run jekyll new
jekyll new .  # at the local repo root
jekyll serve # to compile the website locally

4. commit/push the auto-generated files

5. Theme
jekyll theme example is here https://github.com/jekyll/minima
See README.md and _config.yml

-------------------

6.

upgraded vim to use system clipboard. Ran
brew install vim

This broke some dependencies, so I had to run gem install jekyll again

gem install --user-install jekyll bundler

The Gemfile became incompatible so I had to do a new `jekyll new`

Finally, I added mathjax following instructions here
http://sgeos.github.io/github/jekyll/2016/08/21/adding_mathjax_to_a_jekyll_github_pages_blog.html


