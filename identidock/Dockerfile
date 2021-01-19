FROM python:3.9

RUN groupadd -r uwsgi && useradd -r -g uwsgi uwsgi

# ARG requirements=requirements/development.txt

WORKDIR /app
COPY app /app
COPY requirements.txt /app/requirements.txt
COPY cmd.sh /

RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 9090 9191
USER uwsgi

CMD ["/cmd.sh"]
