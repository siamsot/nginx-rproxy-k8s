FROM python:3-alpine
RUN pip install flask
# if our app was more complex with more dependencies, a requirement.txt file would be used
WORKDIR /app
ADD app.py /app
EXPOSE 8080
ENTRYPOINT [ "python" ]
CMD [ "app.py" ]
