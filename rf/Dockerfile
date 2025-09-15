FROM rapidfort/python-chromedriver
RUN pip install --no-cache-dir semgrep
RUN apt-get update && \
    apt-get install -y --no-install-recommends git && \
    rm -rf /var/lib/apt/lists/*
ENV PATH="/home/nonroot/.local/bin:${PATH}"

WORKDIR /src
ENTRYPOINT ["semgrep"]
