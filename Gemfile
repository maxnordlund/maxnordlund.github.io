source "https://rubygems.org"

require "json"
require "open-uri"
versions = JSON.parse(open("https://pages.github.com/versions.json").read)

gem "github-pages", versions["github-pages"]

group :test do
  gem "html-proofer"
  gem "rubocop"
  gem "mdl"
end
