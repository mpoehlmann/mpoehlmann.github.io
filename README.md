# mpoehlmann.github.io

Michael Poehlmann's personal website.

- https://github.com/Phlow/feeling-responsive
- https://github.com/artemsheludko/flexible-jekyll

## Initial setup

### Prerequisites
Install the prerequisites:

```bash
brew install ruby
brew --prefix ruby
export PATH=/opt/homebrew/opt/ruby/bin:$PATH
# export PATH=$(gem environment gemdir)/bin:$PATH
export PATH=/Users/michael/.gem/ruby/3.1.0/bin:$PATH
gem install --user-install bundler jekyll
```

### Local testing

When first downloading the code, run

```bash
npm install
bundle install
```

to install the necessary NPM packages and gems for the project.

To create a local server, run

```bash
bundle exec jekyll serve
```


## Tutorial

### Installing bootstrap
Installing bootstrap: https://simpleit.rocks/ruby/jekyll/tutorials/how-to-add-bootstrap-4-to-jekyll-the-right-way/

```bash
npm init --force
npm install bootstrap@5.2 jquery popper.js @fortawesome/fontawesome-free
# npm install --save @fortawesome/fontawesome-free
```

To `_config.yml` add:
```yaml
sass:
  load_paths:
    - _sass
    - node_modules
include:
  - ".htaccess"
  - "node_modules"
  - "_pages"
exclude:
  - "Gemfile"
  - "Gemfile.lock"
  - "vendor/bundle/"
  - "vendor/cache/"
  - "vendor/gems/"
  - "vendor/ruby/"
```

To `_includes/default.html` add:
```html
<html>
<body>
...
	<script src="{{'/node_modules/jquery/dist/jquery.min.js' | prepend: site.baseurl}}"></script>
	<script src="{{'/node_modules/popper.js/dist/umd/popper.min.js' | prepend: site.baseurl}}"></script>
	<script src="{{'/node_modules/bootstrap/dist/js/bootstrap.min.js' | prepend: site.baseurl}}"></script>
</body>
</html>
```

To `_sass/custom.scss` add:
```scss
@import "base/variables";
@import "base/mixins";
@import "bootstrap/scss/bootstrap";
@import "fortawesome/fontawesome-free/scss"
```
Note that bootstrap is imported AFTER the custom variables and mixins, so they override the bootstrap defaults.

## Debugging liquid

This employs the [jekyll-debug](https://github.com/gemfarmer/jekyll-debug) plugin.
To use, add the `debug` filter:
```liquid
{{ site | debug }}
```

### Project structure

The minimum project structure a Jekyll-based website are:

- `_includes/`
  - `head.html`: The `<head>` section for each HTML page.
- `_layouts/`
  - `default.html`: The default HTML layout for a page.
- `Gemfile`:
- `index.md` or `index.html`: The main page of the website.

The `index.md` file contains the following yaml lines at the top, which selects the file in `_layout/` to define the theme:

```yaml
---
layout: default
---
```

The `default.html` file contains the following lines, which includes the `head.html` file:

```html
<!DOCTYPE html>
<html lang="en">
{% include head.html %}
<body>

  <div class="wrapper">
    {{ content }}
  </div>

</body>
</html>
```

### Website additions

### Adding a new page

### Adding a new section to a page


## TODO

- [ ] Favicons
- [ ] `tags.html`
- [ ] `gulpfile.js`
- [ ] Set one link to `active` in `nav.html


### Structure
- [ ] `index.html`
  - [x] `_layouts/home.html`
    - [x] header
  - [x] `_layouts/page.html`
  - [ ] `_layouts/default.html`
  - [ ] `_includes/head.html`
  - [ ] `_includes/nav.html`
  - [ ] `_includes/footer.html`

- [ ] Tooltips
- [ ] Bugs with active being removed from nav
- [ ] Submenu with page sections


## TODO
- [ ] citations: https://pages.lip6.fr/Pascal.Poizat/blog/posts/2016/02/01/jekyll-and-bibtex/
- [ ] Deploy: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- [ ] Some cookies are misusing the recommended “SameSite“ attribute

- [x] `_includes/footer_scripts.html`
- [ ] `_includes/footer.html`
- [x] `_includes/head.html`
- [ ] `_includes/navbar.html`
- [ ] `_layouts/default.html`
- [ ] `_layouts/page.html`

aside -> sidebar
footer
section
contact