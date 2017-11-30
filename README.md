# docker-rails-config
Docker config files to spin up Rails app

After cloning into the folder in which you want your rails app, run -

  ```
  $ docker-compose build web
  $ docker-compose run web rails new . -T --force --skip-turbolinks --skip-coffee-script --database=postgresql
  $ docker-compose run web rake db:create
  $ docker-compose run web rake db:migrate
  ```
  
Add to Gemfile -

  ```
  gem 'webpacker', '= 3.0.1'
  ```
  
Run -

  ```
  $ docker-compose run web rake webpacker:install
  $ docker-compose run web rake webpacker:install:react
  $ docker-compose up
  ```

  
  
