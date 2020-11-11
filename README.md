# Casper Light Fr 

[![Known Vulnerabilities](https://snyk.io/test/github/ziedzaiem/Casper-Light-Fr/badge.svg?targetFile=package.json)](https://snyk.io/test/github/ziedzaiem/Casper-Light-Fr?targetFile=package.json)

A french 🇫🇷 translated light theme for [Ghost](http://github.com/tryghost/ghost/) based on [Casper](https://github.com/TryGhost/Casper).


## Screenshots

<img src="https://raw.githubusercontent.com/ziedzaiem/Casper-Light-Fr/master/Screenshots/homepage.png" width="100" alt="homepage.png" />

<img src="https://raw.githubusercontent.com/ziedzaiem/Casper-Light-Fr/master/Screenshots/post.png" width="100" alt="post.png" />

<img src="https://raw.githubusercontent.com/ziedzaiem/Casper-Light-Fr/master/Screenshots/author.png" width="100" alt="author.png" />

<img src="https://raw.githubusercontent.com/ziedzaiem/Casper-Light-Fr/master/Screenshots/tag.png" width="100" alt="tag.png" />

## Download

Get the last release from the [releases tab](https://github.com/ziedzaiem/Casper-Light-Fr/releases).

## Important ❗

Personal links to other social accounts are added to the following files :

- [default.hbs](default.hbs#L40)
- [partials/site-nav.hbs](partials/site-nav.hbs#L32)
- [post.hbs](post.hbs#L117)

You should delete theme if you want to compile thes theme yourself. They have been deleted from the release 0.0.1.

## Local Development

You need to have NodeJS and npm installed, plus :

```shell
npm install -g yarn@latest
npm install -g ghost-cli@latest
npm install -g gulp-cli@latest
npm install -g nodemon@latest
npm install -g gscan@latest
```

Install a local copy of Ghost by:

```shell
cd .. && mkdir local-ghost && cd local-ghost
ghost install local
```

Setup and configure [Ghost](http://localhost:2368/ghost/) and stop it when finished:

```shell
ghost stop
```

Create a symlink for the current project in the content/themes/ directory:

```shell
ln -s $PWD/../Casper-Light-Fr content/themes/Casper-Light-Fr
```

Launch Ghost with nodemon :

```shell
nodemon current/index.js --watch content/themes/Casper-Light-Fr --ext hbs,js,css
```

### Run development server

Casper-Light-Fr styles are compiled using Gulp/PostCSS to polyfill future CSS spec. You'll need [Node](https://nodejs.org/), [Yarn](https://yarnpkg.com/) and [Gulp](https://gulpjs.com) installed globally. After that, from the theme's root directory:

```bash
# install dependencies
yarn install

# run development server
yarn dev
```

Now you can edit `/assets/css/` files, which will be compiled to `/assets/built/` automatically.

### Compile the theme

The `zip` Gulp task packages the theme files into `dist/<theme-name>.zip`, which you can then upload to your site.

```bash
# create .zip file
yarn zip
```

## Validate the theme

Use [gscan](https://github.com/TryGhost/gscan) to checks for errors and feature support :

```
gscan . --verbose -3
```

## iconmonstr icons

The following icons are made by [iconmonstr](https://iconmonstr.com/) :

- [partials/github.hbs](partials/github.hbs)
- [partials/gmail.hbs](partials/gmail.hbs)
- [partials/instagram.hbs](partials/instagram.hbs)
- [partials/linkedin.hbs](partials/linkedin.hbs)


## How to compare with original project

```
git remote add -f casper https://github.com/TryGhost/Casper.git
git remote update
git diff master remotes/casper/master
git remote rm casper

```