FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y \
    ruby-full \
    build-essential \
    zlib1g-dev \
    git \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /srv/jekyll
COPY . /srv/jekyll

RUN gem install bundler -v 2.4.22
RUN bundle install
RUN jekyll build

EXPOSE 4000

CMD ["jekyll", "serve", "--host", "0.0.0.0", "--watch", "--incremental"]
