FROM python:3.14.8-slim

RUN pip install --no-cache-dir \
      "dlt[ducklake,s3]==1.31.0" \
      "duckdb==1.5.6" \
      "zstandard==0.25.0" \
    && useradd --uid 1000 --create-home --home-dir /home/loader --shell /usr/sbin/nologin loader

USER 1000
ENV HOME=/home/loader

RUN python -c "import duckdb; c = duckdb.connect(); [c.install_extension(e) for e in ('httpfs', 'postgres_scanner', 'ducklake')]"
