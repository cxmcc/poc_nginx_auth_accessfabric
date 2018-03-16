# poc_nginx_auth_accessfabric
POC for scaleft's accessfabric nginx module (https://github.com/ScaleFT/nginx_auth_accessfabric) (build scripts)
The script handles mostly the build for nginx binary with the nginx module. 

## How to run this
```sh
$ docker-compose up --build
Starting pocnginxauthaccessfabric_app_1 ... 
Starting pocnginxauthaccessfabric_app_1 ... done
Starting pocnginxauthaccessfabric_nginx_1 ... 
Starting pocnginxauthaccessfabric_nginx_1 ... done
Attaching to pocnginxauthaccessfabric_app_1, pocnginxauthaccessfabric_nginx_1
app_1    |  * Running on http://0.0.0.0:8080/ (Press CTRL+C to quit)
app_1    |  * Restarting with stat
app_1    |  * Debugger is active!
app_1    |  * Debugger PIN: 297-164-724
```

## What's not done here
* SSL termination to nginx endpoint.
* Other obvious configurations.
