require 'rake'
require 'rake/testtask'
require 'rake/rdoctask'

require 'lib/tasks/list_tests.rb'

# Test::Unit::UI::VERBOSE

Rake::TestTask.new do |t|
  t.libs << 'lib'
  t.pattern = 'test/{unit,functional,other}/**/*_test.rb'
  t.verbose = false
end

Rake::RDocTask.new { |rdoc|
  rdoc.rdoc_dir = 'doc'
  rdoc.title    = "Shoulda -- Making your tests easy on the fingers and eyes"
  rdoc.options << '--line-numbers' << '--inline-source'
  rdoc.template = "#{ENV['template']}.rb" if ENV['template']
  rdoc.rdoc_files.include('README', 'lib/**/*.rb')
}

desc 'Default: run tests.'
task :default => ['test']