FROM cassandra:2.1

RUN apt-get update -y && \
    apt-get install -y curl  sudo  && \
    echo "deb http://debian.datastax.com/community stable main" | tee -a /etc/apt/sources.list.d/datastax.community.list && \
    curl -L https://debian.datastax.com/debian/repo_key | apt-key add - && \
    apt-get update -y && \
    apt-get install -y datastax-agent && \
    apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

COPY docker-entrypoint.sh /docker-entrypoint.sh
