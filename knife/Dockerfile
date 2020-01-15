FROM ruby:slim

RUN mkdir -p /knife
WORKDIR /knife
VOLUME /knife
RUN set -ex                                              \
    && buildDeps='libgmp3-dev gcc make'                  \
    && apt update                                        \
    && apt upgrade -y                                    \
    && apt install -y --no-install-recommends $buildDeps \
    && rm -rf /var/lib/apt/lists/*                       \
    && gem install chef --version '~>12'                 \
    && apt purge -y --auto-remove $buildDeps
RUN gem install bundler:1.17.1
ENTRYPOINT ["knife"]
CMD ["--help"]
