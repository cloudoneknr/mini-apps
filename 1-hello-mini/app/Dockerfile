FROM python:3.9-alpine
WORKDIR /app
RUN pip install Flask
COPY . .
EXPOSE 5000
CMD ["python", "hello.py"]