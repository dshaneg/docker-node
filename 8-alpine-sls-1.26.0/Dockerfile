FROM dshaneg/nodejs:8-alpine

LABEL "MAINTAINER" "shane.gibbons@gmail.com"

RUN apk -v --update add \
        python \
        py-pip \
        groff \
        less \
        mailcap \
        jq \
        && \
    pip install --upgrade awscli==1.14.32 s3cmd==2.0.1 python-magic && \
    apk -v --purge del py-pip && \
    rm /var/cache/apk/*

RUN yarn global add serverless@1.26.0
