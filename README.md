Personal-Website
================

## Running The Site
1) Assuming docker/nginx is setup, if not, do so.
2) docker stop $(docker ps -a -q) - Note use a specific name if you have multiple builds running
3) docker rm $(docker ps -a -q)
4) docker build . -t personal-website
5) docker run -td --name personal-website -p 8080:80 -v $(pwd):/usr/share/nginx/html nginx
