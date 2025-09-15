FROM cgr.dev/chainguard/python:latest-dev AS builder
RUN python3 -m pip install --no-cache-dir --user semgrep

FROM cgr.dev/chainguard/git:latest AS git

# Stage 2: production (minimal distroless)
FROM cgr.dev/chainguard/python:latest
# copy all git binary
COPY --from=git /usr/bin/git /usr/bin/git
COPY --from=git /usr/libexec/git-core /usr/libexec/git-core
COPY --from=git /lib/ /lib/
COPY --from=git /usr/lib/ /usr/lib/
# Copy all Python libraries and binaries from builder
COPY --from=builder /home/nonroot/.local/lib/python3.13/ /home/nonroot/.local/lib/python3.13/
COPY --from=builder /home/nonroot/.local/bin/ /home/nonroot/.local/bin/
COPY --from=builder /usr/lib/python3.13/site-packages /usr/lib/python3.13/site-packages
ENV PATH="/home/nonroot/.local/bin:${PATH}"

WORKDIR /src
ENTRYPOINT ["semgrep"]
