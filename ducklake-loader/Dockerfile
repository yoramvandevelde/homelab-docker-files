# dlt loader for the homelab DuckLake: raw-events-v2 (Silo) into DuckLake with a Postgres catalog.
# The loader script itself comes from a ConfigMap in gitops-v2 (apps/duckdb).
# Slim, not Alpine: duckdb publishes no musl wheel, so Alpine would mean building DuckDB from source.
FROM python:3.14.8-slim

RUN pip install --no-cache-dir \
      "dlt[ducklake,s3]==1.31.0" \
      "duckdb==1.5.6" \
      "zstandard==0.25.0" \
    && useradd --uid 1000 --no-create-home --shell /usr/sbin/nologin loader

USER 1000
