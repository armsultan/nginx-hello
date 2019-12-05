
# NGINX webserver and test page

Simple backends for various load balancing demos.

NGINX webserver that serves a simple page containing its hostname, IP address 
and port as wells as the request URI and the local time of the webserver.

Based on -- https://hub.docker.com/r/nginxdemos/hello/

How to run:
```
# HTML page
$ docker run -P -d nginxdemos/hello

# HTML Coffee page
$ docker run -P -d nginxdemos/hello:coffee

# HTML Tea page
$ docker run -P -d nginxdemos/hello:coffee

# HTML Tea page
$ docker run -P -d nginxdemos/hello:plain-text
```

## Hello

Now, assuming we found out the IP address and the port that mapped to port 80 on the container, in a browser we can make a request to the webserver and get the page below:

![hello](hello.png)

## Coffee and Tea

Other HTML variations include are a coffee and tea page:
![coffee](coffee.png)
![tea](tea.png)

## Plain Text

Lastly, a plain text version of the image is available as `nginxdemos/hello:plain-text`. This version returns the same information in the plain text format:
```
$ curl <ip>:<port>
Server address: 172.17.0.2:80
Server name: 22becba5323d
Date: 07/Feb/2018:16:05:05 +0000
URI: /
Request ID: 48ba0db334a6ed165e783469c2af868f
```