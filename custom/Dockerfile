FROM alpine:3.20

ENV LIBRARY_PATH=/lib:/usr/lib
RUN apk add --update --no-cache \
	gcc \
	g++ \
	make \
	ruby-dev \
	ruby \
	asciidoctor \
	python3 && \
    gem install --no-document asciidoctor-pdf --pre && \
    gem install --no-document coderay pygments.rb && \
    gem cleanup && \
    apk del \
    	gcc \
    	g++ \
    	make \
    	ruby-dev && \
    rm -rf /tmp/* /var/cache/apk/* ~/.cache/pip

WORKDIR /documents
VOLUME /documents

CMD ["/bin/sh"]
