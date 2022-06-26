# docker exercice
docker run -d-it -v /MountPoint --name myalpes alpine /bin/ash
docker start myalpes
docker attach myalpes
echo "WARNING: ret pointer is null" > test.py
docker commit myalpes myalpine:v12
docker export myalpes > myfile.tar
#docker rmi -f $(docker images -q)    
cat myfile.tar | docker import - myalpine:v12
docker history myalpine:v12
docker login -u <docker_hub_account> -p <password>
docker image tag myalpine:v12 <docker_hub_account>/myalpine:v12
docker push <docker_hub_account>/myalpine