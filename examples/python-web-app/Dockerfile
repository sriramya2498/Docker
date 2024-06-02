FROM ubuntu

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

ENV pip_break-system-packages 1 
RUN apt-get update && \
    python3 -m pip install -r requirements.txt &&\
    cd devops

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




