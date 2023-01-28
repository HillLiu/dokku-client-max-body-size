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

# If you don't need a global client_max_body_size, you should try it with official way.
* https://dokku.com/docs/networking/proxies/nginx/#specifying-a-custom-client_max_body_size
```
dokku nginx:set [app-name] client-max-body-size 100m
dokku ps:rebuild [app-name] 
```
* unset it
```
dokku nginx:set [app-name] client-max-body-size
dokku ps:rebuild [app-name] 
```
