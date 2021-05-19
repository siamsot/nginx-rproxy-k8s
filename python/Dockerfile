FROM python:3-alpine # Using alpine as it is faster and smaller
RUN pip install flask
# if our app was more complex with more dependencies, a requirement.txt file would be used
WORKDIR /app
ADD app.py /app
EXPOSE 5000 #exposing this for testing for now
ENTRYPOINT [ "python" ]
CMD [ "app.py" ]
