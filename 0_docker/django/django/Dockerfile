FROM python:3.11.6

WORKDIR /usr/src/app

COPY . .

RUN python -m pip install --upgrade pip
RUN pip install -r requirements.txt


# CMD python manage.py runserver 0.0.0.0:8000
# gunicorn을 사용하기 위해 주석처리

# WORKDIR ./myapp
# CMD gunicorn --bind 0.0.0.0:8000 myapp.wsgi:applicationdocker
# 비정상 종료로 주석처리

CMD gunicorn --chdir /usr/src/app/myapp --bind 0.0.0.0:8000 myapp.wsgi:application

EXPOSE 8000
