# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...




Running_app_in_production_locally

1. Add `gem 'rails_12factor'` to your Gemfile. This will add error logging and the ability for your app to serve static assets. 
1. `bundle`
1. Run `RAILS_ENV=production rake db:create db:migrate db:seed`
1. Run `rake secret` and copy the output
1. From the command line: `export SECRET_KEY_BASE=output-of-rake-secret`
1. To precompile your assets, run `rake assets:precompile`. This will create a folder `public/assets` that contains all of your assets.
1. Run `RAILS_ENV=production rails s` and you should see your app. 

Remember to clobber your assets (`rake assets:clobber`) and re-precompile (`rake assets:precompile`) if you make changes. 

To compile assets in production mode (with css_compressor, :uglifier or other js_compressor):
`rake assets:precompile RAILS_ENV=production`