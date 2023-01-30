FROM public.ecr.aws/amazonlinux/amazonlinux
ARG FUNCTION_DIR="/opt/backend/"
RUN yum -y update; yum -y install python3-pip
RUN pip3 install fastapi uvicorn
RUN mkdir -p ${FUNCTION_DIR}
WORKDIR ${FUNCTION_DIR}
COPY app/* ${FUNCTION_DIR}
EXPOSE 80
CMD uvicorn main:app --host 0.0.0.0 --port 80
