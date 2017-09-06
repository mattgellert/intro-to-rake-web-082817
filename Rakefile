desc 'outputs hello to the terminal'
task :hello do
  puts "hello from Rake!"
end

namespace :greeting do
  desc "prints out 'hello from Rake!'"
  task :hello do
    puts "hello from Rake!"
  end

  desc "prints out 'hola de Rake!'"
  task :hola do
    puts "hola de Rake!"
  end

end

namespace :db do
  desc "gives access to config/environment"
  task :environment do
    require_relative './config/environment'
  end

  desc "invokes the :environment task as a dependency"
  task :migrate => :environment do
    Student.create_table
  end

  desc "fills the database with dummy data"
  task :seed => :environment do
    require_relative './db/seeds.rb'
  end

end
