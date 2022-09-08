FROM ruby:2.2

ENV APP_HOME /app
ENV POST_SERVICE_HOST post
ENV POST_SERVICE_PORT 5000
ENV COMMENT_SERVICE_HOST comment
ENV COMMENT_SERVICE_PORT 9292

RUN mkdir $APP_HOME
WORKDIR $APP_HOME

RUN apt-get update -qq \
    && apt-get install -y build-essential \
    && rm -r /var/lib/apt/lists/*

COPY Gemfile* $APP_HOME/
RUN bundle install
COPY . $APP_HOME

CMD ["puma"]
