ARG PYTHON_VERSION=3.9
FROM python:${PYTHON_VERSION}-slim AS builder

# Install semgrep into /usr/local (instead of ~/.local)
RUN pip install --no-cache-dir --prefix=/usr/local semgrep

# Install git
RUN apt-get update && \
    apt-get install -y --no-install-recommends git && \
    rm -rf /var/lib/apt/lists/*

# Stage 2: production (minimal distroless)
FROM gcr.io/distroless/python3-debian12

# copy git
COPY --from=builder /usr/bin/git /usr/bin/git
COPY --from=builder /usr/lib/git-core /usr/lib/git-core
ARG PYTHON_VERSION=3.9
# copy semgrep + site-packages
COPY --from=builder /usr/local/bin/ /usr/local/bin/
COPY --from=builder /usr/local/lib/ /usr/local/lib/
COPY --from=builder /lib/ /lib/
COPY --from=builder /usr/local/lib/python${PYTHON_VERSION}/site-packages /usr/local/lib/python${PYTHON_VERSION}/site-packages

ENV PYTHONPATH=/usr/local/lib/python${PYTHON_VERSION}/site-packages
ENV PATH="/usr/local/bin:${PATH}"

WORKDIR /src
ENTRYPOINT ["semgrep"]
