# docker-rails-config
Docker config files to spin up Rails app

After cloning into the folder in which you want your rails app, run -

  docker-compose build web
  docker-compose run web rails new . -T --force --skip-turbolinks --skip-coffeescript --database=postgresql --webpacker=react
  
  
