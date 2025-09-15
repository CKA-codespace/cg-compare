FROM vulnfree.dev/public/python-alpine:latest
RUN pip install --no-cache-dir semgrep
RUN apk add --no-cache git
ENV PATH="/home/nonroot/.local/bin:${PATH}"

WORKDIR /src
ENTRYPOINT ["semgrep"]
