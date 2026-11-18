FROM python:3.14.8-slim

RUN pip install --no-cache-dir \
      "dlt[pyiceberg,s3]==1.32.0" \
      "pyiceberg==0.12.0" \
      "zstandard==0.25.0" \
    && useradd --uid 1000 --create-home --home-dir /home/loader --shell /usr/sbin/nologin loader

USER 1000
ENV HOME=/home/loader
