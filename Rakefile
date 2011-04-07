
namespace :web do
  desc "Update the Github website"
  task :update do
    system "rocco Git-enterprise"
    system "git checkout web"
    system "mv Git-enterprise.html index.html"
    system "git add index.html && git co -m 'Updated Git-enterprise website'"
    system "git push"
    system "git checkout master"
  end

end
