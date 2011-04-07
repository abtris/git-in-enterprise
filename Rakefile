
namespace :web do
  desc "Update the Github website"
  task :update do
    system "rocco Git-enterprise"
    system "git checkout web"
    system "mv Git-enterprise.html index.html"
    system "git add ." 
	system "git commit -m 'Updated Git-enterprise website'"
    system "git push origin web:gh-pages"
	system "git checkout master"
  end

end
