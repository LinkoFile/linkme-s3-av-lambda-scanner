# linkme-s3-av-lambda-scanner

1. setup clamav layer using Docker and upload it as a lambda layer

docker run --rm -v "$PWD":/tmp lambci/yumda:2 sh -c \
  'yum install -y clamav && cd /lambda/opt && zip -yr /tmp/layer.zip .'

2. zip src folder and upload it as lambda functions source code
3. set up handlers, events and environment variables as in sam .yaml files from the directory
4. set up layer for both functions