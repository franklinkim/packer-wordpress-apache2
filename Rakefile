require 'colorize'

task :default do
  system "rake -T"
end

desc "Validate template.json"
task :validate do |t|
  puts "Validating template...".light_yellow
  system "packer validate template.json"
end

desc "Update all submodules to the latest tag"
task :update do |t|
  puts "Current status...".light_yellow
  system "git submodule status"
  puts "Updating submodules...".light_yellow
  system "git submodule foreach 'git fetch origin; git checkout $(git describe --tags `git rev-list --tags --max-count=1`);'"
end

desc "Build from template.json"
task :build do |t|
  puts "Building box...".light_yellow
  system "packer build template.json"
end

desc "Add a built box to vagrant"
task :add, [:name, :path]  do |t, args|
  puts "Adding box #{args.name} from #{args.path}".light_yellow
  system "vagrant box add --name #{args.name} #{args.path}"
end
