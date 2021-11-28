FROM debian
RUN apt-get update -y && apt-get install -y git python-pip
RUN git clone https://github.com/josedom24/gestion.git
WORKDIR gestion
RUN pip install --no-cache-dir -r requirements.txt
RUN mkdir basededatos
COPY BD/db2020.sqlite3 basededatos/db.sqlite3
COPY index.html templates/index.html
COPY conf/* ./

CMD [ "python", "manage.py","runserver","0.0.0.0:8000" ]
