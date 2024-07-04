require_relative 'lib/bddsm/version'
# require 'bundler/gem_tasks'

task :release do
  version = BDDSM::VERSION
  sh "gem build bddsm-test.gemspec"
  sh "git add -A"
  sh "git commit -m 'Release version #{version}'"
  sh "git tag v#{version}"
  sh "git push origin v#{version}"
  sh "gem push bddsm-test-#{version}.gem"
end