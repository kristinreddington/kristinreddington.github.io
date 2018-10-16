---
layout: post
title:      "Rails & React tips & tricks "
date:       2018-10-16 04:03:31 +0000
permalink:  rails_and_react_tips_and_tricks
---


I love building full-stack apps using rails api and react for the front end. The two frameworks were seemingly made for each other and it's very easy to manipulate JSON with both tools, making transfering data less of a headache. Of course, without the right organization, it's easy to get messy...fast. Learning and mastering common best practices has made developing not only easier but more fun throughout the process.  I thought I'd provide a few little tricks I've picked up along the way that will provide ease to work flow. 

* Set up a rake task so you can start the servers from a single command 

If you're using port 3000 for your app, proxy your rails api to port 3001 and install the gem 'foreman'. Bundle install and create a Procfile.dev file and paste: 

eb: cd client && PORT=3000 npm start
api: PORT=3001 && bundle exec rails s

In your lib/tasks directory, create a new file, start.rake. Use this code to create a development rake task that you can load up your server with a simple 'rake start' command instead of running two different terminal windows for your seperate ports: 

namespace :start do
  desc 'Start dev server'
  task :development do
    exec 'foreman start -f Procfile.dev'
  end
end


task :start => 'start:development' 

Now you're good to go with a 'rake start'! 

* Create an initializer to create your own API from an third party API. 

If you're working with a third party API for data with your own app, but want to create your own database with data for security or because of CORS limitations, etc., a good idea is to build an initializer that will fetch the data you need and store it in your own API upon loading the server. Use gem 'rest-client' to make a simple get request from your chosen API, and some logic to add new data that hasn't been saved to the database yet. For example, using recipepuppy's simple, you could create your own API by adding this file into your initializers folder: 

require 'rest-client'
require 'rails/configuration'

recipe_puppy_url = "http://www.recipepuppy.com/api/"

data = JSON.parse( RestClient.get("#{recipe_puppy_url}") )

data["results"].each do |recipe, index|
  existing_recipe = Recipe.find_by(:title => recipe["title"])

  if !existing_recipe

    new_recipe = Recipe.new do |attr|
      attr.title = recipe["title"]
      attr.url = recipe["url"]
      attr.ingredients = recipe["ingredients"]
      attr.image = recipe["thumbnail"]
    end

    if new_recipe.save
      puts "recipe saved"
    else
      puts "recipe not saved"
      end
    end
  end
	
	
* 	Use helpers - a lot! 

This is especially true if you're not using a front end framework and decide to implement rails' built in views. Cohesion may not be followed tightly in React, but in Rails it's best to leave all logic out of the views. If you have different navigation links for when a user is logged in and logged out, think about making partials for the different views and inside the navigation partial, use a helper method that loads either one depending on if the user is authorized or not. This will make your code cleaner, easier to debug and follows the single responsibility principal. 



