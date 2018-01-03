# cdev

FROM alpine
LABEL Description="Sets up a C development environment"
RUN ["apk", "update"]
RUN ["apk", "upgrade"]
RUN ["apk", "add", "man", "man-pages", "mdocml-apropos", "less", "less-doc"]
ENV PAGER less
RUN ["apk", "add", "bc"]
RUN ["apk", "add", "vim"]
RUN ["apk", "add", "vim-doc"]
RUN ["apk", "add", "gcc"]
RUN ["apk", "add", "gcc-doc"]
RUN ["apk", "add", "musl-dev"]
RUN ["apk", "add", "make"]
RUN ["apk", "add", "make-doc"]
RUN ["apk", "add", "git"]
RUN ["apk", "add", "git-doc"]
RUN ["apk", "add", "valgrind"]
RUN ["apk", "add", "valgrind-doc"]
RUN ["apk", "add", "tmux"]
RUN ["apk", "add", "tmux-doc"]
COPY .profile /root/
COPY .vimrc /root/
WORKDIR /projects
ENTRYPOINT ["/bin/ash", "-l"]
