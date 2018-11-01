# Mule ESB Dockerfile
Docker Image packaging for MuleESB http://www.mulesoft.org


## How to use
```
docker pull m9rcy/mule
```

### Usage

For a simple application using 8081 port as HTTP

```
docker run -d --name myMuleInstance -P -v ~/myAppsDir:/opt/mule/apps -v ~/myLogsDir:/opt/mule/logs m9rcy/mule
```

#### Noteworthy mount points

| Mount point       | Description                                                     |
|------------------ |-----------------------------------------------------------------|
|/opt/mule/apps     | Mule Application deployment directory                           |
|/opt/mule/domains  | Mule Domains deployment directory                               |
|/opt/mule/conf     | Configuration directory                                         |
|/opt/mule/logs     | Logs directory                                                  |


#### Exposed ports

| Port | Description                                                     |
|----- |-----------------------------------------------------------------|
| 8081 | Default HTTP port                                               |


This means only exposed port is 8081, if the application has other needs you should use `-p` rather than `-P` 

```
-p 1234:1234
````

### Tips

Use docker inspect to identify the ip address or use docker machine and let it assign the localhost to all container in a standard way.

