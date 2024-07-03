FROM python:3.9-alpine
WORKDIR /app
LABEL org.opencontainers.image.description="vote"\
    org.opencontainers.image.authors="CristianSigel"
ENV PORT 80
COPY requirements.txt /app
RUN pip install -r requirements.txt
COPY . /app
EXPOSE 80
CMD [ "python", "app.py" ]