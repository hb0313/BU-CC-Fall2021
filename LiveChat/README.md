# CS552 - Cloud Computing
## _Miniproject-2_

[![N|Solid](.images/BU-LockupH-WatsonCollege-342.png)](https://www.binghamton.edu/computer-science/index.html)

Microservices and Orchestration via building a simple two-tier live chat microservices and deploy it in Minikube.

## Steps

#### Live chat on native:

```
    #Start Mongodb in background
    $ sudo mongod --bind_ip=0.0.0.0 &
    #Run the webserver
    $ python3 run.py
```
- Navigate to http://external_ip:8080/

### Live chat using docker container:
```
#Start mongodb container
$ cd mongodb
$ sudo make run
#Start webserver container
$ cd webserver
$ sudo make run
```

### Live chat using minikube
