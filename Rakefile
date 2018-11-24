require "rspec/core/rake_task"

RSpec::Core::RakeTask.new(:spec)

task :default => :spec

$LOAD_PATH.unshift("#{__dir__}/lib")
require "ayashige"

desc "Fetching domains via WebAnalyzer"
task :fetch_from_webanalyzer do
  puts "Fetching domains via WebAnalyzer..."
  job = Ayashige::Jobs::CronJob.new
  job.perform
  puts "done."
end
