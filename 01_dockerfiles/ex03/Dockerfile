# bacon strips

FROM debian
LABEL Description="Builds and deploys the latest development version of Gogs"
RUN ["apt-get", "update"]
RUN ["apt-get", "install", "-y", "git"]
RUN ["apt-get", "install", "-y", "golang"]
RUN ["apt-get", "install", "-y", "sqlite3"]
ENV USER root
ENV GOPATH /
WORKDIR src/github.com/gogits
RUN ["git", "clone", "--depth=1", "-b", "develop", "https://github.com/gogits/gogs"]
RUN ["go", "get", "-u", "-tags", "sqlite", "github.com/gogits/gogs"]
WORKDIR gogs
RUN ["go", "build", "-tags", "sqlite"]
EXPOSE 3000
ENTRYPOINT ["./gogs", "web"]
