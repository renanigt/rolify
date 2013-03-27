source "https://rubygems.org"

case ENV["ADAPTER"]
when nil, "active_record"
  group :test do
    gem "activerecord-jdbcsqlite3-adapter", :platform => "jruby"
    gem "sqlite3", :platform => "ruby"
  end
  gem "activerecord", ">= 3.2.0", :require => "active_record"
when "mongoid"
  gem "mongoid", ">= 3.1"
  gem "bson_ext", :platform => "ruby"
else
  raise "Unknown model adapter: #{ENV["ADAPTER"]}"
end

group :test do
  gem 'coveralls', :require => false
end

gemspec