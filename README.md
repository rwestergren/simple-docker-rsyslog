#simple-docker-rsyslog:
A simple/lightweight rsyslog server meant for debugging. Log messages are sent to stdout for viewing with `docker logs`.

##Quick Start
###Build/Pull the image:
`docker pull rwestergren/simple-docker-rsyslog`

###Run an instance:
`docker run -d --name rsyslog -p 514:514 -p 514:514/udp rwestergren/simple-docker-rsyslog`

###Stream the logs:
`docker logs -f rsyslog`

###Send a test message from another terminal:
`echo "test message" | nc -4u -w1 localhost 514`

You should see the message in your console. Enjoy!
