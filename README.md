# touhottaja.github.io
Personal GitHub pages site.

## Environment
1. Install ruby:`$ sudo apt-get install ruby -ys`
2. Install bundler and [jekyll](https://jekyllrb.com/): `$ gem install --user-install bundler jekyll`
3. Add the following to .bashrc (set the version number): `export PATH=$PATH:~/.gem/ruby/[<Version number>]/bin`
4. cd to the site folder: `$ cd [<Path to repo>]/touhottaja-site`
5. Install missing gems: `$ bundle install`
6. Run the site locally: `$ bundle exec jekyll serve`
7. Navigate to `localhost:4000`
