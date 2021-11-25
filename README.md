# docker-project
The current objective of this project is to use Docker containers to host different games and make them playable from any local web browser.

__To do things:__
- ~~Create another container to host a static webpage that will redirect to any of these games.~~
- Finish the static sample webpage and customize each instance.
- ~~write a docker-compose.yml file to run all the containers at once.~~
- ~~docker-compose written but still unfinished. We need to add lines to the .yml to copy the main page .html inside the web container.~~

Optional objectives (we're not doing these but just in case we have that much time'):
- Add more games
- Make docker-compose able to run in an Azure Container Instance.

# Instructions:
- Clone or download this repository to your PC.
- Install docker and docker-compose, you can find the official docker instructions here: https://docs.docker.com
- Open a Terminal in this directory (path/docker-project) and run:
```
$: docker-compose up
```
- This will download files, build images for the containers, and get them all running. Note: This could take a while the first time, depending on what docker images you already have downloaded in your computer and your internet speed. Next times will take considerably less.

- To stop all containers from running, open another terminal in the same directory and run:
```
$: docker-compose down
```
For now, there's no main website to redirect you to each game, so you'll only be able to access each one by going to:
> Sample website: localhost:80 (only an empty website but it's there to check it's working ok)
> Doom: localhost:81
> Keen: localhost:82
> Cosmo: localhost:83
> Secret Agent: localhost:84
> Prince of Persia: localhost:85
> Infinite Mario Bros: localhost:86
