FROM python:latest

RUN apt-get update && apt-get install -y \
    libgl1 \
    libglib2.0-0 \
    libsm6 \
    libxext6 \
    libxrender-dev \
    && rm -rf /var/lib/apt/lists/*


WORKDIR /app
COPY requirements.txt requirements.txt
RUN pip install -r requirements.txt
COPY receiver.py receiver.py

CMD ["python", "receiver.py"]
