require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  gem.name = "scaffolder"
  gem.homepage = "http://next.gs"
  gem.license = "MIT"
  gem.summary = %Q{Genome scaffolding for human beings.}
  gem.description = %Q{Organise sequence contigs into genome scaffolds using simple human-readable YAML files.}
  gem.email = "mail@next.gs"
  gem.authors = ["Michael Barton"]
  gem.test_files = Dir['test/**/*.rb']
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

require 'cucumber/rake/task'
Cucumber::Rake::Task.new(:features)

require 'yard'
YARD::Rake::YardocTask.new

task :default => :test
