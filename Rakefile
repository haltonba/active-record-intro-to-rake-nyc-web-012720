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

desc "connects to environment.rb"
  task :environment do
    require_relative './config/environment.rb'
  end
  
desc "drop into pry console"
  task :console => :environment do
    Pry.start
  end
  
namespace :db do
  desc "migrates changes to database"
    task :migrate => :environment do
      Student.create_table
    end
  desc "seeds database with dummy data"
    task :seed => :environment do
      require_relative './db/seeds.rb'
    end
end


