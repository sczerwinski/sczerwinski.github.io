# Run Jekyll with `bundle exec`, like so:
#     bundle exec jekyll serve --incremental --livereload

source "https://rubygems.org"

gem "github-pages", "~> GITHUB-PAGES-VERSION", group: :jekyll_plugins
gem "webrick"

group :jekyll_plugins do
  gem "jekyll-paginate"
  gem "jekyll-redirect-from"
end

platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1.0", :platforms => [:mingw, :x64_mingw, :mswin]
