FROM jekyll/jekyll:4.2.2

RUN gem update --system 3.3.22
RUN bundle update --bundler

WORKDIR /srv/jekyll
COPY . /srv/jekyll

RUN gem install bundler -v 2.4.22
RUN bundle install
RUN jekyll build

EXPOSE 4000
CMD ["jekyll", "serve", "--host", "0.0.0.0"]
