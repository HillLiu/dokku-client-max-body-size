# Dokku Nginx client-max-body-size plug-in

## Install
```
sudo dokku plugin:uninstall client-max-body-size \
  || sudo dokku plugin:install https://github.com/hillliu/dokku-client-max-body-size.git
```

## Set global
```
dokku config:set --global client_max_body_size=100M
```

## Set local 
```
dokku config:set [app-name] client_max_body_size=100M
```
