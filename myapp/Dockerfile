FROM ruby:2.3
ENV LANG C.UTF-8
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs npm mysql-client

ENV APP_HOME /myapp
RUN mkdir $APP_HOME
WORKDIR $APP_HOME

ADD Gemfile* $APP_HOME/
#RUN bundle install --path=$APP_HOME/vendor/bundle --jobs 10 --retry 5
RUN bundle install

ADD . $APP_HOME

#EXPOSE 3000
#CMD ["bundle", "exec", "unicorn", "-c", "config/unicorn.rb"]
