# Darren Bot
This is a python chatbot that is made using rasa.
## How to run
First run a following command to launch a docker image
```
docker run -d -p 5005:5005 -p 5002:5002 -p 80:80 -p 8888:8888 --name rasa -e GRANT_SUDO=yes --user root -e JUPYTER_ENABLE_LAB=yes -v %cd%:/home/jovyan cliffweng/cory
```

After the docker container is up and running,run the following command in the container prompt
```
git clone https://github.com/julianweng/mybot.git
cd mybot
rasa train
rasa run actions &
rasa x
```