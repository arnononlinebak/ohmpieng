require 'recap/recipes/static'

set :deploy_to, "/var/config"
server 'ohmpieng.org', :app
set :user, 'non'
set :use_sudo, true
set :application, "config"
set :application_user, 'non'
set :repository,  "git@bitbucket.org:nonmadden/config.git"

after 'deploy', 'deploy:reload'

namespace :deploy do
  task :reload, roule: :app do
    run 'sudo service nginx reload'
  end

  task :setup, roule: :app do
  	run "sudo rm -rf /etc/nginx/sites-enabled/default"
  	run "sudo ln -s /var/config/default /etc/nginx/sites-enabled/default"
    run "sudo nginx -t"
    run "sudo service nginx start"
  end
end
