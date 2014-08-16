require 'recap/recipes/static'

set :application, "config"
set :application_user, 'non'
set :repository,  "git@bitbucket.org:arnononline/config.git"
set :deploy_to, "/home/non/config"
set :user, 'non'
server 'ohmpieng.org', :app

run 'sudo service nginx reload'
