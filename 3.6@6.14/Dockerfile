From node:6.14
Maintainer Wang Sheng <shengw1127@gmail.com>

# install node-gyp
RUN apt-get update \
    && apt-get install --no-install-recommends -y python build-essential openjdk-7-jdk unzip \
    && apt-get clean
RUN npm install -g node-gyp@3.6
RUN npm install -g node-sass@4.8

USER node
ENV SONAR_SCANNER_CLI_VERSION=3.0.3.778
RUN curl --insecure -o ~/sonar-scanner-cli.zip -sSL https://sonarsource.bintray.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-${SONAR_SCANNER_CLI_VERSION}-linux.zip \
    && mkdir -p ~/.sonar/native-sonar-scanner/ \
    && unzip -qq ~/sonar-scanner-cli.zip -d ~/.sonar/native-sonar-scanner/ \
    && rm -f ~/sonar-scanner-cli.zip
