source "https://rubygems.org"

# Core Jekyll. We use plain Jekyll 4.3 instead of the github-pages gem because
# github-pages pins Jekyll 3.9 + Liquid 4.0.3, which calls the removed `tainted?`
# method and crashes on Ruby 3.2+/4.x.
gem "jekyll", "~> 4.3"

# Liquid 4.0.4 removed the `tainted?`/`untaint` calls (needed for Ruby 4).
# Pin explicitly so bundler never resolves back down to 4.0.3.
gem "liquid", "~> 4.0.4"

# Minimal Mistakes is used via remote_theme (needs jekyll-remote-theme)
gem "jekyll-remote-theme"
gem "jekyll-include-cache"

# Plugins declared in _config.yml
# (bundled by github-pages before; must be declared explicitly now)
gem "jekyll-paginate"
gem "jekyll-sitemap"
gem "jekyll-gist"
gem "jemoji"

# Required for Ruby 3.4+ as these gems are no longer bundled
gem "csv"
gem "webrick"
gem "bigdecimal"

# Required by jekyll-remote-theme with Faraday v2+
gem "faraday-retry"

# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :windows, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1", :platforms => [:windows]