#
# Haproxy Dockerfile
#
# https://github.com/dockerfile/haproxy
#

# Pull base image.
FROM dockerfile/ubuntu

# Install Haproxy.
RUN \
  add-apt-repository ppa:vbernat/haproxy-1.5 && \
  apt-get update && \
  apt-get install -y haproxy && \
  sed -i 's/^ENABLED=.*/ENABLED=1/' /etc/default/haproxy

# Add files.
ADD haproxy.cfg /etc/haproxy/haproxy.cfg
ADD bundle.cunninghamshane.com.pem /etc/ssl/bundle.cunninghamshane.com.pem
ADD start.bash /haproxy-start

# Define mountable directories.
VOLUME ["/data", "/haproxy-override"]

# Define working directory.
WORKDIR /etc/haproxy

# Define default command.
CMD ["bash", "/haproxy-start"]

# Expose ports.
EXPOSE 80
EXPOSE 443
