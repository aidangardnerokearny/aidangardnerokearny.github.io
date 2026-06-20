source "https://rubygems.org"

# The github-pages gem pins Jekyll + all whitelisted plugins to the exact
# versions GitHub's servers run, so "works locally" == "works deployed".
gem "github-pages", group: :jekyll_plugins

# Plugins used by this template (also whitelisted on GitHub Pages)
group :jekyll_plugins do
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
end

# Windows / JRuby helpers — harmless to keep on macOS/Linux
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end
gem "wdm", "~> 0.1.1", platforms: [:mingw, :x64_mingw, :mswin]
gem "http_parser.rb", "~> 0.6.0", platforms: [:jruby]
