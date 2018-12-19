namespace :greeting do
  desc 'outputs hello to the terminal'
    task :hello do
      puts "hello from Rake!"
    end

  desc 'outputs hola to the terminal'
    task :hola  do
      puts "hola de Rake!"
  end
end

tasks hello & hola are under namespace greeting


task :environment do
  require_relative './config/environment'
  #does it matter where this goes?^
  #environment must be defined for :migrate => environment below
end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end
  #namespace = way to group/contain something
end
