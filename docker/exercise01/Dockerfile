FROM debian
ARG FUNCTION_DIR="/opt/backend/"
RUN apt-get update; apt-get -y full-upgrade
RUN apt-get -y install python3-pip
RUN pip3 install fastapi uvicorn
RUN mkdir -p ${FUNCTION_DIR}
WORKDIR ${FUNCTION_DIR}
COPY app/* ${FUNCTION_DIR}
EXPOSE 8000
CMD uvicorn main:app --host 0.0.0.0 --port 8000
