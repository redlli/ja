source "https://rubygems.org"

# Core Jekyll and Layout Engine (Told to grab latest available)
gem "jekyll"
gem "liquid"

# Force eventmachine to use a stable version compatible with Ruby 3.3+ and OpenSSL 3
gem "eventmachine", ">= 1.2.7"

# Jekyll Plugins
group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
end

# Windows and JRuby environment configurations
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo"
  gem "tzinfo-data"
end

gem "wdm", :platforms => [:mingw, :x64_mingw, :mswin]
gem "http_parser.rb", :platforms => [:jruby]
