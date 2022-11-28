FROM python:3

RUN useradd -m -d /app backend
RUN apt-get update

RUN python -m pip install flask
COPY ./ /app

# ENV STUDENT_NAME="Leo Li"
# ENV STUDENT_ID="A01226711"

WORKDIR /app
USER root
RUN chmod +x student_create.sh

USER backend
EXPOSE 5000

ENTRYPOINT [ "/bin/bash", "/app/student_create.sh" ]
CMD python3 web.py