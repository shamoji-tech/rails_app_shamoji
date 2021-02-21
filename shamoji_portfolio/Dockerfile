FROM ruby:2.5.8-buster

WORKDIR /root/

RUN apt-get -yqq update && apt-get -yqq upgrade \
  && apt-get install -y \
    less \
    nodejs \
    postgresql-client \
    yarn
    

WORKDIR /myapp

COPY Gemfile Gemfile
COPY Gemfile.lock Gemfile.lock
RUN gem install bundler:2.2.11 && bundler install --without test development
EXPOSE 3000
COPY . /myapp

CMD ["bundle", "exec", "rails", "server", "-b", "0.0.0.0"]