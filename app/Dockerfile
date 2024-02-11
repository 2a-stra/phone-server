FROM python:3.9.10-alpine

RUN pip3 install flask gunicorn

WORKDIR /home/app

COPY ./templates ./templates
COPY ./app.py .

EXPOSE 8888

#CMD ["python", "app.py"]
CMD ["gunicorn", "--bind", "0.0.0.0:8888", "app:app"]