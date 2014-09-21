require 'recap/recipes/static'

set :deploy_to, "/var/config"
server 'ohmpieng.org', :app
set :user, 'root'
set :use_sudo, true
set :application, "config"
set :application_user, 'root'
set :repository,  "git@bitbucket.org:nonmadden/config.git"

after 'deploy', 'deploy:reload'

namespace :deploy do
  task :reload, roule: :app do
    run 'sudo service nginx reload'
  end

  task :setup, roule: :app do
    run "sudo cp /var/config/config/php-fpm /etc/nginx/"
    run 'sudo service nginx start'
  end
end
