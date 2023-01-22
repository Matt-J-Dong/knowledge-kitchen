![Deploy to i6 badge](https://github.com/bloombar/amos-web-site/actions/workflows/deploy.yml/badge.svg)

# Personal web site

Code to generate and automatically deploy a simple personal website.

## Deployed site

View the [deployed site](https://knowledge.kitchen).

## Running locally

The code in this repository is used to generate the website using [jekyll](https://jekyllrb.com/) and continuously deploy it using a [GitHub Actions](https://github.com/features/actions) workflow.

It is possible to run the website locally on your own machine.

- Assuming [Ruby](https://www.ruby-lang.org/en/documentation/installation/) is installed...
- Install [Jekyll](https://jekyllrb.com/) globally
- Install the dependencies listed in the `Gemfile` by running the command, `bundle`.
- run `bundle exec jekyll serve` or simply `jekyll serve` if that doesn't work.
