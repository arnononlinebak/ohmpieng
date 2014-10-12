require 'recap/recipes/static'

set :deploy_to, "/var/config"
server 'ohmpieng.org', :app
set :user, 'non'
set :use_sudo, true
set :application, "config"
set :application_user, 'non'
set :repository,  "https://arnononline:f537b1ff0bd7298dee49257f4c8de1191207d8b8@github.com/arnononline/ohmpieng.git"

after 'deploy', 'deploy:reload'

namespace :deploy do
  task :reload, role: :app do
    run "sudo nginx -t"
    run 'sudo service nginx reload'
  end
end
