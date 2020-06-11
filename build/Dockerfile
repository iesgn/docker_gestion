FROM python:2.7.16-stretch
RUN apt-get update -y && apt-get install -y git 
RUN git clone https://github.com/josedom24/gestion.git
WORKDIR gestion
RUN pip install --no-cache-dir -r requirements.txt
COPY BD/* ./
CMD [ "python", "manage.py","runserver","0.0.0.0:8000" ]