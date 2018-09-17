# Capistrano gem

https://github.com/capistrano/capistrano

# Capistrano rbenv

https://github.com/capistrano/rbenv

# edit deploy.rb

```
set :application, "pumadeploy"
set :repo_url, "git@github.com:wangsy/pumadeploy.git"

set :rbenv_type, :user
set :rbenv_ruby, '2.5.1'

set :deploy_to, "/home/wangsy/pumadeploy"

append :linked_files, "config/database.yml"

append :linked_dirs, "log", "tmp/pids", "tmp/cache", "tmp/sockets", "public/system"

```

# edit deploy/staging.rb

```
server "pumadeploy", user: "wangsy", roles: %w{app db web}
```

# push to github

# first deploy

`bundle exec cap staging deploy`

# Capistrano puma

https://github.com/seuros/capistrano-puma

`bundle exec cap staging puma:config`
`cap production puma:nginx_config
`
