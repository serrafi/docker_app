FROM alpine:3.5
RUN apk add --update py2-pip
RUN pip install --upgrade pip
WORKDIR /app
COPY app /app
COPY cmd.sh /
EXPOSE 9090

CMD ["/cmd.sh"]
