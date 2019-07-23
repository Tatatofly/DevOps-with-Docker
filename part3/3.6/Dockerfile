FROM ruby:2.6.0
EXPOSE 3000
WORKDIR /app
COPY Gemfile Gemfile.lock ./
COPY . .
RUN bundle config --global frozen 1 && \
    gem install bundler && \
    bundle install && \
    chmod 777 /tmp && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    rails db:migrate && \
    apt-get purge -y --auto-remove curl && \
    rm -rf /var/lib/apt/lists/* && \
    useradd -m app && \
    chown -R app /app /tmp
USER app
ENTRYPOINT rails s
