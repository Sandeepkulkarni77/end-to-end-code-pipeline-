FROM public.ecr.aws/amazonlinux/amazonlinux:2022

RUN yum install -y python3 && \
    curl -O https://bootstrap.pypa.io/get-pip.py && \
    python3 get-pip.py && \
    pip3 install --upgrade pip

WORKDIR /app

COPY requirements.txt .
RUN pip3 install -r requirements.txt

COPY . .

ENV FLASK_APP=app.py
ENV PLATFORM=AmazonECS

EXPOSE 5000

CMD ["python3", "app.py"]

