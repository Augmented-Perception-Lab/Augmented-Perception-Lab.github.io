# Website for the Augmented Perception Lab at CMU HCII

Deployed at https://augmented-perception.org/.

Based on the website of the CMU Data Interaction Group (https://dig.cmu.edu/), which is open source on Github (https://github.com/cmudig).

## Usage

Install Jekyll dependencies with `bundle`. To start this page, run `bundle exec jekyll serve --livereload`.

To add specific content, follow the README guides in the corresponding directories:

* [Add a person](_people)
* [Add a publication](_publications)
<!-- * [Add a post](_posts) -->

### Known issues

- If site disappears from https://augmented-perception.org, make sure that the website in Settings/Pages/Custom domain is not blank (should be https://augmented-perception.org)

#### Jekyll broken (Mac)
- *Could not find concurrent-ruby-1.1.7 in any of the sources*
- *listen-3.2.1 requires ruby version >= 2.2.7, ~> 2.2, which is incompatible with the current version, ruby 3.0.0p0*

**Resolution**: MacOS probably broke your Jekyll installation (`jekyll --version` yields an error, ruby version no longer compatible). Try `gem install listen` and `bundle update` in the directory of the site. If this does not help, follow install steps again (https://jekyllrb.com/docs/installation/macos/).

## Pushing an update

1. Check out the site via github
2. Make change and check correctness via above bundle command
3. Push to Github

The site is published automatically through a Github workflow.

## Useful links for the theme:

https://tachyons.io/#style

https://tachyons.io/docs/layout/spacing/

https://tachyons.io/docs/typography/line-height/
