FROM python:3.8-bullseye
RUN pip3 install atheris

COPY . /marko
WORKDIR /marko
RUN python3 -m pip install . && chmod +x fuzz/marko_fuzz.py

ENTRYPOINT [ ]
CMD ["/marko/fuzz/marko_fuzz.py"]