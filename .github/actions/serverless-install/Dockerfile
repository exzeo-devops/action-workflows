FROM alpine:3.12

# Install NodeJS by version 20.x
RUN apk add --no-cache nodejs npm

# Install Python and PIP
RUN apk add --no-cache python3 py3-pip

# Install AWS CLI and Serverless Linting
RUN pip3 install awscli cfn-lint cfn-lint-serverless

# Install Serverless Framework
RUN npm install -g serverless
