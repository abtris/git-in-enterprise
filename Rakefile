
namespace :web do
  desc "Update the Github website"
  task :update do
    system "rocco Git-enterprise"
    current_branch = `git branch --no-color`.split("\n").select { |line| line =~ /^\* / }.to_s.gsub(/\* (.*)/, '\1')
    (puts "Unable to determine current branch"; exit(1) ) unless current_branch
    system "git stash && git checkout web && git stash pop"
    system "mv Git-enterprise.html index.html"
    system "git add index.html && git co -m 'Updated Git-enterprise website'"
    system "git push origin web:gh-pages -f"
    system "git checkout #{current_branch} && git stash pop"
  end

end
