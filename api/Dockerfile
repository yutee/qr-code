FROM python:3.9-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install -r requirements.txt

COPY . .

ENV AWS_ACCESS_KEY=secrets.AWS_ACCESS_KEY
ENV AWS_SECRET_KEY=secrets.AWS_SECRET_KEY

EXPOSE 8000

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]

