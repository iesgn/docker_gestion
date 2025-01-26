FROM debian:12
RUN apt-get update && apt-get install -y python3-pip libcairo2-dev pkg-config python3-dev  libpango-1.0-0 libpangoft2-1.0-0 && apt-get clean && rm -rf /var/lib/apt/lists/*
WORKDIR /usr/share/app
COPY gestion_py3 .
RUN pip install --no-cache-dir --break-system-packages -r requirements.txt
COPY conf/* ./
EXPOSE 8000
CMD [ "python3", "manage.py","runserver","0.0.0.0:8000" ]
