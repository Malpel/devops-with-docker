FROM ruby:2.6.0
WORKDIR /usr/src/app
COPY Gemfile Gemfile.lock ./
RUN gem install bundler
RUN bundle install
COPY . .
RUN apt-get update && apt-get install -y nodejs
RUN EDITOR="nano --wait" bin/rails credentials:edit
RUN rails db:migrate RAILS_ENV=production
RUN rake assets:precompile
EXPOSE 3000
CMD ["rails", "s", "-e", "production"]

