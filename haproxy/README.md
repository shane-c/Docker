## from dockerfile/haproxy

Usage

docker run -d -p 80:80 dockerfile/haproxy
Customizing Haproxy

docker run -d -p 80:80 -v <override-dir>:/haproxy-override dockerfile/haproxy
where <override-dir> is an absolute path of a directory that could contain:

haproxy.cfg: custom config file (replace /dev/log with 127.0.0.1, and comment out daemon)
errors/: custom error responses
