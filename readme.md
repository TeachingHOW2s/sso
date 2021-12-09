# TeachingHOW2s SSO Docs

## Installation

Documentation is generated with [mkdocs-material](https://github.com/squidfunk/mkdocs-material) which can be installed via Docker:

    docker pull squidfunk/mkdocs-material

## Development

To start a local dev server run:

    docker run --rm -it -p 8090:8000 -v ${PWD}:/docs squidfunk/mkdocs-material

## Manual Builds

    docker run --rm -v ${PWD}:/docs squidfunk/mkdocs-material build

## Deployment

GitHub pages will automatically update whenever commits are pushed.
