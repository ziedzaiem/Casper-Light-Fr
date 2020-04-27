# Casper Light Fr

A french 🇫🇷 translated light theme for [Ghost](http://github.com/tryghost/ghost/) based on [Casper](https://github.com/TryGhost/Casper).

## Screenshots

![](Screenshots/homepage.png | width=100)

![](Screenshots/post.png | width=200)

![](Screenshots/author.png | width=200)

![](Screenshots/tag.png | width=200)

## Download

Get the last release from the [releases tab](https://github.com/ziedzaiem/Casper-Light-Fr/releases).

## Note

Personal links to other social accounts are added to the following files :

- [default.hbs](default.hbs#L40)
- [partials/site-nav.hbs](partials/site-nav.hbs#L32)

You should delete theme if you want to compile thes theme yourself. They have been deleted from the release.

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
