# srechallenge
Run a web server through Docker, Dockerfile, docker build, docker run

```
Yukuis-MacBook:srechallenge Yukui_Ye$ ls
Dockfile	index.html
Yukuis-MacBook:srechallenge Yukui_Ye$ mv Dockfile Dockerfile
Yukuis-MacBook:srechallenge Yukui_Ye$ ls
Dockerfile	index.html
Yukuis-MacBook:srechallenge Yukui_Ye$ docker build -t srechallenge .
Sending build context to Docker daemon 3.072 kB
Step 1/2 : FROM nginx:alpine
 ---> 7ebd6770d0d6
Step 2/2 : COPY index.html /usr/share/nginx/html
 ---> 5fe1c364c876
Removing intermediate container 23e4b74f6cb5
Successfully built 5fe1c364c876
Yukuis-MacBook:srechallenge Yukui_Ye$ docker run -p 9000:80 srechallenge
172.17.0.1 - - [02/Jun/2017:22:24:02 +0000] "GET / HTTP/1.1" 200 110 "-" "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_12_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/58.0.3029.110 Safari/537.36" "-"

```
