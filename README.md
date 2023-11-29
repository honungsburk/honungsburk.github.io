# Honungsburk - Website

The official homepage of honnungsburk (a.k.a. Frank Hampus Weslien).

## Static Site Generation

I use [Zola](https://www.getzola.org/) to build this static site.

### Installation

Follow the [instructions](https://www.getzola.org/documentation/getting-started/installation/).

### Development

Get instant refresh using `zola serve`.

Note: It appears that the site becomes unavailable after deployment. Thus far
all I've had to do are the following steps:

1. Go to the [settings page for this repo](https://github.com/honungsburk/honungsburk.github.io/settings)
2. Click on the [pages tab](https://github.com/honungsburk/honungsburk.github.io/settings/pages)
3. Under Custom domain write "frankhampusweslien.com" and click Save.

### Deployment

Whenever changes get committed to the `master` branch it triggers a Github action
that builds and deploys the website to the `gh-pages` branch.

## Styling

### Fonts

We use JetBrains Mono for that great programmer _feel_.

### Icons

We use Feather for this project. If you need an icon that has not been added
simply navigate to their [website](https://feathericons.com/) and download it!

### Sass

You find the sass file at `sass/style.sass`.
