require 'jekyll'
namespace :computerfarmer do
  desc 'Delete generated _site files'
  task :clean do
    system "rm -fR _site"
  end

  desc 'Run the jekyll dev server'
  task :server do
    system "jekyll serve --watch --detach"
  end

  desc 'Clean temporary files and run the server'
  task :compile do
    system "jekyll build"
  end

  desc 'Push to s3'
  task :deploy do
    system "s3_website push"
  end
end

task :default => ["computerfarmer:compile"]