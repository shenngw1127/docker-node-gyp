From node:6.13
Maintainer Wang Sheng <shengw1127@gmail.com>

# install node-gyp
RUN apt-get update \
    && apt-get install --no-install-recommends -y python build-essential openjdk-7-jdk unzip \
    && apt-get clean
RUN npm install -g node-gyp@3.6
RUN npm install -g node-sass@4.8

ARG sonar-scanner-cli-version=3.1.0.1141-linux
RUN curl -sSL -o /tmp/sonar-scanner-cli.zip https://sonarsource.bintray.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-${sonar-scanner-cli-version}.zip \
    && mkdir -p ~/.sonar/ \
    && unzip /tmp/sonar-scanner-cli.zip -d ~/.sonar/ \
    && rm -f /tmp/sonar-scanner-cli.zip
