From node:6.13
Maintainer Wang Sheng <shengw1127@gmail.com>

# install node-gyp
RUN apt-get update \
    && apt-get install --no-install-recommends -y python build-essential openjdk-7-jdk \
    && apt-get clean
RUN npm install -g node-gyp@3.6
RUN npm install -g node-sass@4.8
