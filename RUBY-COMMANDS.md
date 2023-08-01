# Ruby

# Rails

create new app
rails new APP_NAME --api

create starter files for entity
rails g scaffold Band name

migrate database
rails db:migrate

run server
rails s

console
rails c


rails g model Member band:references name


rails g scaffold Member --skip-migration
