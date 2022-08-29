desc "Outputs hello to the terminal"
task :hello do
  puts "hello from Rake!"
end

desc "outputs hole to the terminal"
task :hola do
  puts "hola de Rake!"
end

#namespacing rake tasks
namespace :greeting do
  desc "outputs hello to the terminal"
    task :hello do
      puts "hello from Rake!"
    end

  desc "outputs hola to the terminal"
    task :hola do
      puts "hola de Rake!"
    end
end

namespace :db do
  desc "migrate changes to your database"
  task migrate: :environment do   #creates a task dependancy
    Student.create_table
  end

  desc "seed the db with dummy data"
  task seed: :environment do
    require_relative "./db/seeds.rb"
  end
end

task :environment do
  require_relative "./config/environment.rb"
end

desc "drop into Pry console"
task console: :environment do
  Pry.start
end


