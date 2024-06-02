FROM azureuser

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

//ENV pip_break-system-packages 1 
RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    python3 -m venv .venv && \
    source .venv/bin/activate && \
    python3 -m pip install -r requirements.txt && \
    cd devops

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]




