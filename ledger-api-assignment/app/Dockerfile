# FROM python:3.6-slim

# WORKDIR /app

# COPY requirements.txt .
# RUN pip install --no-cache-dir -r requirements.txt

# COPY app.py .

# EXPOSE 8080

# CMD ["python", "app.py"]


FROM python:3.6-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

RUN groupadd --gid 10001 appgroup \
    && useradd \
       --uid 10001 \
       --gid 10001 \
       --no-create-home \
       appuser

COPY . .

RUN chown -R 10001:10001 /app

USER 10001:10001

CMD ["python", "app.py"]
