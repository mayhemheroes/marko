FROM python:3.11-slim

RUN apt-get update && apt-get install -y --no-install-recommends clang && rm -rf /var/lib/apt/lists/*
RUN pip3 install atheris

COPY . /marko
WORKDIR /marko
RUN python3 -m pip install . && chmod +x fuzz/marko_fuzz.py

ENTRYPOINT [ ]
CMD ["/marko/fuzz/marko_fuzz.py"]
