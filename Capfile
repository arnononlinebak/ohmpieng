require 'recap/recipes/static'

set :deploy_to, "/var/config"
server 'ohmpieng.org', :app
set :user, 'non'
set :use_sudo, true
set :application, "config"
set :application_user, 'non'
set :repository,  "https://nonmadden:Arnon007@github.com/nonmadden/ohmpieng.git"

after 'deploy', 'deploy:reload'

namespace :deploy do
  task :reload, role: :app do
    run "sudo nginx -t"
    run 'sudo service nginx reload'
  end
end
