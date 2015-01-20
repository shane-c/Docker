FROM registry

# python-swiftclient requires lxml
RUN apt-get update && apt-get install -yq python-lxml git

RUN git clone https://github.com/bacongobbler/docker-registry-driver-swift.git /src
RUN pip install /src
