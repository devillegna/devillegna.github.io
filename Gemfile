source "https://rubygems.org"

# GitHub Pages builds this site with its own pinned set of gems. Depending on
# the `github-pages` gem alone keeps local builds identical to production: it
# already pins jekyll, kramdown, sass and the supported plugins. Do NOT add an
# explicit `gem "jekyll"` line here -- that fights the pin and breaks
# `bundle install`.
gem "github-pages", group: :jekyll_plugins

gem "wdm", "~> 0.1.0" if Gem.win_platform?

# Ruby 3.x no longer bundles webrick, which `jekyll serve` needs.
gem "webrick", "~> 1.8"

# Plugins. Everything listed here must also appear under `plugins:` in
# _config.yml and be on the GitHub Pages allowlist:
# https://pages.github.com/versions/
group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-sitemap"
  gem "jekyll-gist"
  gem "jekyll-paginate"
  gem "jekyll-redirect-from"
end
