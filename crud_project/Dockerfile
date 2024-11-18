FROM python:3.12-alpine

COPY .env .env

COPY requirements.txt requirements.txt

RUN pip install --no-cache-dir -r requirements.txt

COPY . .

ENV SECRET_KEY=django-insecure-nw^y+m^wmxza1asgk+)!ua2qx9)g+#v=6%76-9i8i(6eqiw94j
ENV DEBUG=True

RUN python manage.py migrate

CMD [ "python", "manage.py", "runserver", "0.0.0.0:8000"]