# poc_nginx_auth_accessfabric
POC for scaleft's accessfabric nginx module (https://github.com/ScaleFT/nginx_auth_accessfabric) (build scripts)
The script handles mostly the build for nginx binary with the nginx module. 

## How to run this
```sh
$ docker-compose up
Starting scaleftnginxaccessfabricpoc_nginx_1 ... 
Starting scaleftnginxaccessfabricpoc_nginx_1
Starting scaleftnginxaccessfabricpoc_app_1 ... 
Starting scaleftnginxaccessfabricpoc_nginx_1 ... done
Attaching to scaleftnginxaccessfabricpoc_app_1, scaleftnginxaccessfabricpoc_nginx_1
app_1    |  * Running on http://0.0.0.0:8080/ (Press CTRL+C to quit)
app_1    |  * Restarting with stat
app_1    |  * Debugger is active!
app_1    |  * Debugger PIN: 297-164-724
```

## What's not done here
* SSL termination to nginx endpoint.
* Other obvious configurations.
