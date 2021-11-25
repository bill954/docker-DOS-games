# docker-project
The objective of this project (for now) is to use containers to host different games and make them playable from a web browser.

To do things:
- ~~Create another container to host a static webpage that will redirect to any of these games.~~
- The container is running ok, but the static webpage is not finished yet.
- ~~write a docker-compose.yml file to run all the containers at once.~~
- docker-compose written but still unfinished. We need to add lines to the .yml to copy the main page .html inside the web container.

Optional objectives (we're not doing these but just in case we have that much time'):
- Add other interesting games (prince of persia maybe)
- Make the docker-compose able to run in Azure Container Instances.

# Instructions:
- Clone or download this repository to your PC.
- Install docker and docker-compose (here you have the official instructions for that: https://docs.docker.com)
- Open a Terminal in this directory (docker-project) and run:
'''
$: docker-compose up
'''
- This will download some files, build images for the containers, and get them all running. This could take a while the first time, depending on what docker images you already have or not in your computer and your internet speed. Next times it will be just a few seconds.

- To stop it all, open another Terminal in this same directory and run:
'''
$: docker-compose down
'''

For now, there still no main website, so you will be able to access each game by going to:

Main website: localhost:80 (only an empty website but it's there to check it's working ok)
Doom: localhost:81
Keen: localhost:82
Cosmo: localhost:83
Secret Agent: localhost:84
Prince of Persia: localhost:85
Mario: localhost:86
