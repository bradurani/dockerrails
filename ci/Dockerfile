FROM bradurani/railsmysql:4.0.0

EXPOSE 3000
ONBUILD ADD . src
ONBUILD WORKDIR /src
ONBUILD RUN bundle install
ONBUILD CMD bundle exec rails server