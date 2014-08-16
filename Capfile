require 'recap/recipes/static'

set :deploy_to, "/home/non/config"
server 'ohmpieng.org', :app
set :user, 'non'
set :use_sudo, true

set :application, "config"
set :application_user, 'non'
set :repository,  "git@bitbucket.org:arnononline/config.git"

after 'deploy', 'deploy:reload'

namespace :deploy do
  task :reload, roule: :app do
    run 'sudo service nginx reload'
  end
end
