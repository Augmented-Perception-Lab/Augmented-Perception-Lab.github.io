# Website for the Augmented Perception Lab at CMU HCII

Deployed at https://augmented-perception.org/.

Based on the website of the CMU Data Interaction Group (https://dig.cmu.edu/), which is open source on Github (https://github.com/cmudig).

## Usage

### Install Jekyll dependencies with `bundle`.  
https://idratherbewriting.com/documentation-theme-jekyll/mydoc_install_jekyll_on_windows.html
1. Install Ruby 2.7.5 with devkit from https://rubyinstaller.org/downloads/ (tested including installing MinGW toolchain)
2. cmd: `gem install jekyll`
3. cmd: `gem install bundler`
4. Clone repository and navigate to it in cmd. Run `bundle install`

### Start page
To start this page, open cmd and navigate to website directory. Then run `bundle exec jekyll serve --livereload`.

To add specific content, follow the README guides in the corresponding directories:

* [Add a publication](_publications)
<!-- * [Add a post](_posts) -->

#### Adding Members

Create an entry in _data/people.yml. Fill it with the following content.

- name: ...
  website: ...
  image: /assets/....jpg
  role: PhD Student
  program: Masters Information Science
  note: Some comment such as school for interns

We have the following roles: `Assistant Professor`, `Administrative coordinator`, `Postdoc`, `PhD Student`, `Visiting PhD student`, `Master's student`, `Undergraduate student`, and `Research Intern`. You can also add a new role in team.html.

Once someone leaves the group, add `alumni_since: XXXX` to move the entry to _data/alumni.yml them as alumni.

## Known issues

- If site disappears from https://augmented-perception.org, make sure that the website in Settings/Pages/Custom domain is not blank (should be https://augmented-perception.org)

#### Jekyll broken (Mac)
- *Could not find concurrent-ruby-1.1.7 in any of the sources*
- *listen-3.2.1 requires ruby version >= 2.2.7, ~> 2.2, which is incompatible with the current version, ruby 3.0.0p0*

**Resolution**: MacOS probably broke your Jekyll installation (`jekyll --version` yields an error, ruby version no longer compatible). Try `gem install listen` and `bundle update` in the directory of the site. If this does not help, follow install steps again (https://jekyllrb.com/docs/installation/macos/).

#### Load error Windows
*C:/Ruby27-x64/lib/ruby/gems/2.7.0/gems/eventmachine-1.2.7-x64-mingw32/lib/rubyeventmachine.rb:2:in `require': cannot load such file -- 2.7/rubyeventmachine (LoadError)*

**Resolution** (https://stackoverflow.com/a/53080143): 
- Go to this folder C:\Ruby24-x64\lib\ruby\gems\2.4.0\gems\eventmachine-1.2.5-x64-mingw32\lib
- open this file eventmachine.rb
- write this `require 'em/pure_ruby'` in the first line of code in the file

## Pushing an update

1. Check out the site via github
2. Make change and check correctness via above bundle command
3. Push to Github

The site is published automatically through a Github workflow.

## Useful links for the theme:

https://tachyons.io/#style

https://tachyons.io/docs/layout/spacing/

https://tachyons.io/docs/typography/line-height/
