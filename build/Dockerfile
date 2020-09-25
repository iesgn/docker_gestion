FROM debian
RUN apt-get update -y && apt-get install -y git python-pip
RUN git clone https://github.com/josedom24/gestion.git
WORKDIR gestion
RUN pip install --no-cache-dir -r requirements.txt
#COPY BD/* ./
COPY conf/* ./
CMD [ "python", "manage.py","runserver","0.0.0.0:8000" ]
