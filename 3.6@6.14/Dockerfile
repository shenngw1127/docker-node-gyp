From node:6.14
Maintainer Wang Sheng <shengw1127@gmail.com>

# install node-gyp
RUN apt-get update \
    && apt-get install --no-install-recommends -y python build-essential openjdk-7-jdk unzip \
    && apt-get clean
RUN npm install -g node-gyp@3.6
RUN npm install -g node-sass@4.8

USER node
ENV SONAR_SCANNER_CLI_VERSION=3.1.0.1141
RUN mkdir -p ~/.sonar/ \
    && curl --insecure -o sonar-scanner-cli.zip -sSL https://sonarsource.bintray.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-${SONAR_SCANNER_CLI_VERSION}-linux.zip \
    && unzip sonar-scanner-cli.zip -q -d ~/.sonar/ \
    && rm -f sonar-scanner-cli.zip
