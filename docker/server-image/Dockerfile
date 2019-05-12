FROM zabbix/zabbix-server-pgsql:ubuntu-3.0-latest

ARG APT_FLAGS_COMMON="-y"
ARG APT_FLAGS_PERSISTENT="${APT_FLAGS_COMMON} --no-install-recommends"

RUN apt-get ${APT_FLAGS_COMMON} update && \
    apt-get ${APT_FLAGS_PERSISTENT} install \
            python \
            python-pip \
            python-setuptools

RUN pip install --no-cache-dir \
            boto3 \
            zabbix-api \
