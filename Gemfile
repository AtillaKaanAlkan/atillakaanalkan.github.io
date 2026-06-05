# This Gemfile is only needed for LOCAL preview.
# GitHub Pages does not use it — it builds the site with its own pinned gems.
source "https://rubygems.org"

gem "github-pages", group: :jekyll_plugins   # matches GitHub Pages' build exactly
gem "webrick", "~> 1.8"                       # needed for `jekyll serve` on Ruby 3+

group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
end
