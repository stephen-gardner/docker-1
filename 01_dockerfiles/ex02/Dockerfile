# ft-rails

FROM ruby
LABEL Description="Containerizes Rails applications."
RUN ["apt-get", "update"]
RUN ["apt-get", "install", "-y", "sqlite3"]
RUN ["apt-get", "install", "-y", "nodejs"]
RUN ["gem", "install", "rails"]
ONBUILD COPY [".", "/opt/app"]
ONBUILD WORKDIR /opt/app
ONBUILD RUN ["bundle", "install"]
ONBUILD RUN ["rails", "db:migrate"]
ONBUILD RUN ["rails", "db:seed"]
ONBUILD EXPOSE 3000
