# Casper Light Fr 

[![Known Vulnerabilities](https://snyk.io/test/github/ziedzaiem/Casper-Light-Fr/badge.svg?targetFile=package.json)](https://snyk.io/test/github/ziedzaiem/Casper-Light-Fr?targetFile=package.json)

A french 🇫🇷 translated light theme for [Ghost](http://github.com/tryghost/ghost/) based on [Casper](https://github.com/TryGhost/Casper).


## Screenshots

<img src="https://raw.githubusercontent.com/ziedzaiem/Casper-Light-Fr/master/Screenshots/homepage.png" width="100" alt="homepage.png" loading="lazy" />

<img src="https://raw.githubusercontent.com/ziedzaiem/Casper-Light-Fr/master/Screenshots/post.png" width="100" alt="post.png" loading="lazy" />

<img src="https://raw.githubusercontent.com/ziedzaiem/Casper-Light-Fr/master/Screenshots/author.png" width="100" alt="author.png" loading="lazy" />

<img src="https://raw.githubusercontent.com/ziedzaiem/Casper-Light-Fr/master/Screenshots/tag.png" width="100" alt="tag.png" loading="lazy" />

## Download

Get the last release from the [releases tab](https://github.com/ziedzaiem/Casper-Light-Fr/releases).

## Important ❗

Personal links to other social accounts and other customisations were added to the source code.

You should delete theme if you want to edit and compile the theme yourself. They have been deleted manually from the release. The have been marked with a ```@TODO``` annotation, you just have to search for this annotation and delete custom code.

**Note** : Members related stuff hasn't been heavily modified, I don't use these feature, I don't know if it works correctly.

## Local Development

You need to have NodeJS and npm installed, plus :

```shell
sudo npm install -g yarn@latest ghost-cli@latest gulp-cli@latest nodemon@latest gscan@latest
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

---

# Original readme.md content :
# Casper

The default theme for [Ghost](http://github.com/tryghost/ghost/). This is the latest development version of Casper! If you're just looking to download the latest release, head over to the [releases](https://github.com/TryGhost/Casper/releases) page.

&nbsp;

![screenshot-desktop](https://user-images.githubusercontent.com/353959/66987533-40eae100-f0c1-11e9-822e-cbaf38fb8e3f.png)

&nbsp;

# First time using a Ghost theme?

Ghost uses a simple templating language called [Handlebars](http://handlebarsjs.com/) for its themes.

This theme has lots of code comments to help explain what's going on just by reading the code. Once you feel comfortable with how everything works, we also have full [theme API documentation](https://ghost.org/docs/api/handlebars-themes/) which explains every possible Handlebars helper and template.

**The main files are:**

- `default.hbs` - The parent template file, which includes your global header/footer
- `index.hbs` - The main template to generate a list of posts, usually the home page
- `post.hbs` - The template used to render individual posts
- `page.hbs` - Used for individual pages
- `tag.hbs` - Used for tag archives, eg. "all posts tagged with `news`"
- `author.hbs` - Used for author archives, eg. "all posts written by Jamie"

One neat trick is that you can also create custom one-off templates by adding the slug of a page to a template file. For example:

- `page-about.hbs` - Custom template for an `/about/` page
- `tag-news.hbs` - Custom template for `/tag/news/` archive
- `author-ali.hbs` - Custom template for `/author/ali/` archive


# Development

Casper styles are compiled using Gulp/PostCSS to polyfill future CSS spec. You'll need [Node](https://nodejs.org/), [Yarn](https://yarnpkg.com/) and [Gulp](https://gulpjs.com) installed globally. After that, from the theme's root directory:

```bash
# install dependencies
yarn install

# run development server
yarn dev
```

Now you can edit `/assets/css/` files, which will be compiled to `/assets/built/` automatically.

The `zip` Gulp task packages the theme files into `dist/<theme-name>.zip`, which you can then upload to your site.

```bash
# create .zip file
yarn zip
```

# PostCSS Features Used

- Autoprefixer - Don't worry about writing browser prefixes of any kind, it's all done automatically with support for the latest 2 major versions of every browser.
- [Color Mod](https://github.com/jonathantneal/postcss-color-mod-function)


# SVG Icons

Casper uses inline SVG icons, included via Handlebars partials. You can find all icons inside `/partials/icons`. To use an icon just include the name of the relevant file, eg. To include the SVG icon in `/partials/icons/rss.hbs` - use `{{> "icons/rss"}}`.

You can add your own SVG icons in the same manner.


# Copyright & License

Copyright (c) 2013-2020 Ghost Foundation - Released under the [MIT license](LICENSE).
