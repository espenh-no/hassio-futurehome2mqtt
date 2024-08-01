ARG BUILD_FROM
FROM $BUILD_FROM

RUN apk add --no-cache python3 py-pip && \
    pip3 install --upgrade pip

# Copy data for add-on
COPY ./ /

RUN pip3 install -r requirements.txt
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
