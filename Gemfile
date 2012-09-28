source 'https://rubygems.org'

gem 'rails',   github: 'rails/rails',   branch: 'master'
gem 'journey', github: 'rails/journey', branch: 'master'
gem 'activerecord-deprecated_finders', github: 'rails/activerecord-deprecated_finders', branch: 'master'


# Bundle edge Rails instead:
# gem 'rails', github: 'rails/rails'

gem 'sqlite3'

# Gems used only for assets and not required
# in production environments by default.
group :assets do
  if false
    gem 'sprockets',       :path => "~/code/gems/sprockets"
    gem 'sprockets-rails', :path => "~/code/gems/sprockets-rails"
  else
    gem 'sprockets',       github: 'ndbroadbent/sprockets',       branch: 'allow_assets_without_processing'
    gem 'sprockets-rails', github: 'ndbroadbent/sprockets-rails', branch: 'dont_recompile_unchanged_assets'
  end

  gem 'sass-rails',      github: 'rails/sass-rails', branch: 'master'
  gem 'coffee-rails',    github: 'rails/coffee-rails', branch: 'master'

  # See https://github.com/sstephenson/execjs#readme for more supported runtimes
  # gem 'therubyracer', platforms: :ruby

  gem 'uglifier', '>= 1.0.3'
end

gem 'jquery-rails'

# To use ActiveModel has_secure_password
# gem 'bcrypt-ruby', '~> 3.0.0'

# To use Jbuilder templates for JSON
# gem 'jbuilder'

# Use unicorn as the app server
# gem 'unicorn'

# Deploy with Capistrano
# gem 'capistrano', group: :development

# To use debugger
gem 'debugger'
