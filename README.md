# mpoehlmann.github.io
Michael Poehlmann's personal website.

Based on the theme [agency-jekyll-theme-starter](https://raviriley.github.io/agency-jekyll-theme-starter/).
Credit to [https://www.orestisgeorgiou.com](https://www.orestisgeorgiou.com) for inspiration as well.


## Local testing
### Initial setup
Install the prerequisites:
```bash
brew install ruby
# To bash_profile, add: export PATH="/Users/michael/.gem/ruby/2.7.0/bin:$PATH"
gem install --user-install bundler jekyll
```


### Testing
When first downloading the code, run 
```bash
bundle install
```
to install the necessary gems for the project.

To create a local server, run
```bash
bundle exec jekyll serve
```

## Adding pages
- add to ``navigation.yml``, match section name in ``sitetext.yml``
- TODO: need to finish


## Google Analytics
### Event tracking
To the hyperlink tag (``<a>``), add:
```html
onclick="gtag('event', 'click', {'event_category':'YourEventCategory', 'event_label':'YourEventLabel'});"
```

My event categories:
- "download": file download from site
- "external": outbound url link click
- "internal": internal link click


## TODO
- colors in style.yml
- add subcations to DarkSide and ARIS-ER
  - DarkSide: A hunt for 5 events over 10 years
- sub pages to add
  - TPC page
  - Dark matter (technical, feyman diagram pic)
  - Dark matter (non-technical, pool ball pic)
- logo, favicon
- header image
- image carousel
- color of buttons/other stuff when first loading page
- picture outlines
- ORCID id by github


## Ideas
- add different headers for each page


## Google
add after head tag
```
<!-- Google Tag Manager -->
<script>(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-5H73CWW');</script>
<!-- End Google Tag Manager -->
```

add after opening body tag
```
<!-- Google Tag Manager (noscript) -->
<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-5H73CWW"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
<!-- End Google Tag Manager (noscript) -->