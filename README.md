# mpoehlmann.github.io

Michael Poehlmann's personal website.

## Tutorial

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

### Initial setup

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
bundle install
```

to install the necessary gems for the project.

To create a local server, run

```bash
bundle exec jekyll serve
```

### Website additions

### Adding a new pae

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


## 