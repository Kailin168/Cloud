FROM python:3

# We copy just the requirements.txt first to leverage Docker cache
COPY ./requirements.txt /app/requirements.txt

WORKDIR /app
# working directory is the directory where the command is executed

RUN pip install --no-cache-dir -r requirements.txt
# when the docker create the image it will install all the requirements in the requirements.txt file

COPY . /app

ENTRYPOINT [ "python" ]

CMD [ "app.py" ]
# the command that will be executed when the container is created
