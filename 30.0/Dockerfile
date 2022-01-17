FROM cimg/android:2021.12.2
ENV PATH="/usr/local/bin/flutter/bin:${PATH}"
# Install and pre-cache Flutter.
RUN wget https://mirror.nju.edu.cn/flutter/flutter_infra/releases/stable/linux/flutter_linux_2.8.1-stable.tar.xz && \
  tar xf flutter_linux_2.8.1-stable.tar.xz -C /usr/local/bin && \
  rm flutter_linux_2.8.1-stable.tar.xz

RUN /usr/local/bin/flutter/bin/flutter precache --no-web --no-linux --no-windows --no-fuchsia --no-ios --no-macos
RUN apt update
RUN apt install -y ruby ruby-dev rubygems
# Install fastlane.
RUN gem install fastlane -NV
