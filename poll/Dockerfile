FROM python
WORKDIR /gilles
ADD requirements.txt /gilles/requirements.txt
RUN pip install -r requirements.txt
ADD . /gilles
EXPOSE 80
CMD flask run --host=0.0.0.0 --port=80