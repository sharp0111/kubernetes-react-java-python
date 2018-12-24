This repository contains all the source files needed to follow the series [Kubernetes and everything else](https://rinormaloku.com/series/kubernetes-and-everything-else/)

This is the best introduction to Kubernetes and Everything related to be able to deploy scalable and resilient applications on Kubernetes managed clusters.

### Serving static files with Nginx
[Instructions on Controlling Nginx](http://nginx.org/en/docs/control.html)\
_OS_ - macOS Mojave
```
username$ brew install nginx
username$ cd /usr/local/etc/nginx
```
Update nginx configuration file:\
`username$ nano nginx.conf`
```
#user your-username;
http {
    server {
        listen          80;
        server_name     localhost;

        location / {
            root        /usr/local/etc/nginx/html;
            index       index.html index.htm;
        }
    }
}
```
Start the server\
`username$ sudo brew services start nginx`

