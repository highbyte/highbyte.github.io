source "https://rubygems.org"

gem "jekyll", "~> 4.3"

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.12"
  gem "jekyll-include-cache"
  gem "jekyll-paginate"
  gem "jekyll-sitemap"
  gem "jekyll-gist"
  gem "jekyll-remote-theme"
  gem "jekyll-titles-from-headings"
end

# tzinfo-data is required on Windows/JRuby; tzinfo 2.x works with Jekyll 4
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", "~> 2.0"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

# webrick was removed from Ruby stdlib in 3.0; needed for jekyll serve
gem "webrick"
