# This is an example of a Rake Task called "hello_rake"
task :hello_rake do
  puts "Hello, from rake"
end

# Define new tasks below
task :default do
	puts "Hello, from default task!"
end

task :environment do
  require_relative './config/environment'
end

task :upcoming_todos => [:environment] do
  User.with_upcoming_todos.each do |user|
    puts "Emailing #{user}"
  end
end

task :overdue_todos => [:environment] do
	User.with_overdue_todos.each do |user|
	  puts "Emailing #{user}"
	end
end