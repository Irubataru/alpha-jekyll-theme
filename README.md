# HTML5 UP "Alpha" - Jekyll Theme

A Jekyll version of the "Alpha" theme by [HTML5 UP](https://html5up.net/).

## Installation

If you are using it with GitHub pages you can simply use it as a [remote
theme][gh-remote] by adding the following to your `_config.yml` file:

``` yml
remote_theme: irubataru/alpha-jekyll-theme
```

An example `_config.yml` and `Gemfile` is located in the [docs](docs) folder.

If you'd rather not use Jekyll remote themes you may also either fork this
repository or copy its contents. In this case you may safely delete

 * docs
 * alpha_jekyll_theme.gemspec
 * README.md
 * LICENSE.txt

## Configuration

As always the main page configuration is through changing the `_config.yml`
file. The theme specific configs are:

``` yml
title: # Name of your webpage
subtitle: # Short name that only appears in the main header
email: # Contact email address
description: # Short description, shown on the home banner

# Social settings
github: mygithub
twitter: mytwittername
facebook: myfacebook
instagram:
dribbble: 
google_plus:
```

The final set of social settings will define which icons show up in the webside
footer.

## Layouts

The theme currently has two main layouts that can be used: `home` and `page`.
These correspond to the landing page of your website and any other site. I'd
generally wish they could be more "jekyll-like", this might be a task for the
future, but for now they rely on you using the `box` environments defined by the
original theme for organisation.

To enable kramdown parsing inside of e.g. a div you can use the

``` html
<div markdown="1">
# An h1 title
Markdown in here
</div>
```

an example of this can be seen in [generic.md](docs/_pages/generic.md).

### The home layout

This is the landing page for your project and is customized with a couple of
jekyll header options:

 * `title` and `description` settings are read from the global configurations
    (in `_config.yml`).
 * `banner_image`: specifies the location of the header image to use
 * `buttons`: is a list of buttons to be placed below the title, they have the
    following options
    - `title`: text on the button
    - `url`: where it points
    - `class`: any optional html classes you want to apply
 * `no_overlay`: toggle whether to overlay the banner image with a blurry filter
    or not
 * `cta`: toggles the CTA banner at the bottom with the following options
    - `title`: title text
    - `description`: descriptive text
    - `field`: placeholder for the text field (default: "Email Address")
    - `action`: text on the button (default: "Sign Up")

### The page layout

For any other page on your website the `page` layout should be used. It has the
following options

 * `title`: main header text
 * `subtitle`: optional descriptive text
 * `box_width`: width of the outer box, defined the with of the page, given as a
   %

## Navigation

The top navigation is generated through the site `site.navigation.main` jekyll
varible. This can be set by editing `_data/navigation.yml`. To generate the
demo navigation this would look like:

``` yml
main:
  - title: Home
  - title: Layouts
    children:
      - title: Generic
        url: /generic
      - title: Contact
        url: /contact
      - title: Elements
        url: /elements
      - title: Submenu
        children:
          - title: "Option 1"
          - title: "Option 2"
          - title: "Option 3"
          - title: "Option 4"
  - title: Sign up
    class: button
```

## Credits

Original README from HTML5 UP:

```
Alpha by HTML5 UP
html5up.net | @ajlkn
Free for personal and commercial use under the CCA 3.0 license (html5up.net/license)


A clean, super minimal responsive template geared towards startups, app devs, and other
dedicated folks working tirelessly to launch their products. Includes a landing page,
generic page, contact page, and a page with a whole mess of pre-styled elements (something
new I'm trying out). Sass sources are also included.

Demo images* courtesy of Unsplash, a radtastic collection of CC0 (public domain) images
you can use for pretty much whatever.

(* = Not included)

Feedback, bug reports, and comments are not only welcome, but strongly encouraged :)

AJ
aj@lkn.io | @ajlkn

PS: Not sure how to get that contact form working? Give formspree.io a try (it's awesome).


Credits:

	Demo Images:
		Unsplash (unsplash.com)

	Icons:
		Font Awesome (fortawesome.github.com/Font-Awesome)

	Other:
		jQuery (jquery.com)
		html5shiv.js (@afarkas @jdalton @jon_neal @rem)
		CSS3 Pie (css3pie.com)
		background-size polyfill (github.com/louisremi)
		Respond.js (j.mp/respondjs)
		Skel (skel.io)

```

[gh-remote]: https://blog.github.com/2017-11-29-use-any-theme-with-github-pages/
