source 'https://rubygems.org'

# Specify the global dependencies in puppetlabs_spec_helper.gemspec
# Note that only ruby 1.9 compatible dependencies may go there, everything else needs to be documented and pulled in manually, and optionally by everyone who wants to use the extended features.
gemspec

group :development do
  puppetver = ENV['PUPPET_GEM_VERSION'] || ENV['PUPPET_VERSION'] || '~> 4.0'

  gem 'puppet', puppetver,       require: false
  gem 'simplecov', '~> 0',       require: false
  if RUBY_VERSION >= '2.1'
    gem 'rubocop', '< 0.50',     require: false
    gem 'rubocop-rspec', '~> 1', require: false
  end
end

# json_pure 2.0.2 added a requirement on ruby >= 2. We pin to json_pure 2.0.1
# if using ruby 1.x
gem 'json_pure', '<=2.0.1', require: false if RUBY_VERSION =~ /^1\./
gem 'rack', '~> 1',         require: false

# vim:filetype=ruby
