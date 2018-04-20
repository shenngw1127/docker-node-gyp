From node:6.14
Maintainer Wang Sheng <shengw1127@gmail.com>

# install node-gyp
RUN apt-get update \
    && apt-get install --no-install-recommends -y python build-essential openjdk-7-jdk unzip \
    && apt-get clean
RUN npm install -g node-gyp@3.6
RUN npm install -g node-sass@4.8

USER node
ARG sonar-scanner-cli-version=3.1.0.1141
RUN curl --insecure -o ~/sonar-scanner-cli.zip -L https://sonarsource.bintray.com/Distribution/sonar-scanner-cli/sonar-scanner-cli-${sonar-scanner-cli-version}-linux.zip
RUN ls -al ~/
RUN mkdir -p ~/.sonar/ \
    && unzip ~/sonar-scanner-cli.zip -d ~/.sonar/
RUN rm -f ~/sonar-scanner-cli.zip
