require 'html-proofer'

task :test do
  sh "bundle exec jekyll build"
  options = { assume_extension: true, verbose: true, url_ignore: [ %r(crateandbarrel\.com) ]  }
  HTMLProofer.check_directory("./_site", options).run
end

task default: :test
