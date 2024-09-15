FROM python:3-bookworm
RUN git clone https://github.com/iesgn/gestion_py3.git /usr/share/app
WORKDIR /usr/share/app
RUN pip install --no-cache-dir -r requirements.txt
COPY conf/* ./
EXPOSE 8000
CMD [ "python", "manage.py","runserver","0.0.0.0:8000" ]
