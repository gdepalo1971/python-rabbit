# python-rabbit

Running the daemon

$ docker run -d --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:management
$ docker logs rabbitmq
Default user and password: guest / guest

$ docker run -d --hostname my-rabbit --name some-rabbit -e RABBITMQ_DEFAULT_USER=user -e RABBITMQ_DEFAULT_PASS=password rabbitmq:3-management
$ docker run -d --hostname my-rabbit --name some-rabbit -e RABBITMQ_DEFAULT_VHOST=my_vhost rabbitmq:3-management
$ docker run -d --hostname my-rabbit --name some-rabbit rabbitmq:3-management
$ docker run -d --hostname my-rabbit --name some-rabbit -p 8080:15672 rabbitmq:3-management

sudo rabbitmqctl list_queues
rabbitmqctl.bat list_queues (Windows)

python -m pip install pika --upgrade

python receive.py
python send.py