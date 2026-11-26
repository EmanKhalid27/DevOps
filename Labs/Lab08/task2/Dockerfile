FROM ubuntu
LABEL maintainer="emankhalidek.01@gmail.com"
RUN sed -i 's|http://security.ubuntu.com/ubuntu|http://archive.ubuntu.com/ubuntu|g' /etc/apt/sources.list
RUN apt-get update --fix-missing && apt-get install -y python3
ENV PAGE_TITLE="DevOps"
WORKDIR /app
RUN echo "<title>$PAGE_TITLE</title><h1>I am a DevOps engineer</h1>" > index.html
EXPOSE 3000
CMD ["python3", "-m", "http.server", "3000", "--bind", "0.0.0.0"]
