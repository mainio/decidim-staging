# frozen_string_literal: true

source "https://rubygems.org"

ruby RUBY_VERSION

DECIDIM_VERSION = { git: "https://github.com/decidim/decidim", branch: "develop" }

gem "decidim", DECIDIM_VERSION
#gem "decidim-conferences", DECIDIM_VERSION
#gem "decidim-consultations", DECIDIM_VERSION
gem "decidim-elections", DECIDIM_VERSION
#gem "decidim-initiatives", DECIDIM_VERSION
#gem "decidim-templates", DECIDIM_VERSION

#gem "webpacker", "6.0.0.rc.5"

# Required with Ruby 3.1.1
gem "stringio", "3.0.1"

gem "wicked_pdf"
gem "wkhtmltopdf-binary"

gem "faker", "~> 2.14"

gem "puma"

gem "letter_opener_web", "~> 1.4.0"
gem "rexml", "~> 3.2.5"

group :development, :test do
  gem "byebug", platform: :mri
end

group :development do
  gem "decidim-dev", DECIDIM_VERSION
  gem "listen", "~> 3.7.1"
  gem "spring"
  gem "spring-watcher-listen", "~> 2.0.0"
  gem "web-console"
end

group :production, :staging do
  gem "dotenv-rails", "~> 2.1", ">= 2.1.1"

  gem "resque", "~> 2.0.0"
  gem "resque-scheduler", "~> 4.4"

  # Cronjobs
  gem "whenever", require: false
end
