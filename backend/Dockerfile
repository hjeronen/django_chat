FROM python:3.8-slim-bullseye
ENV PYTHONUNBUFFERED=1
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
RUN python manage.py migrate
EXPOSE 8000
CMD daphne -b 0.0.0.0 -p 8000 backend.asgi:application