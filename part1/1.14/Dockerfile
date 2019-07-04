FROM ruby:2.6.0
EXPOSE 3000
RUN bundle config --global frozen 1
WORKDIR .
COPY Gemfile Gemfile.lock ./
RUN gem install bundler
RUN bundle install
COPY . .
RUN chmod 777 /tmp
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN rails db:migrate
ENTRYPOINT rails s
