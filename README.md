# docker-project

The current objective of this project is to use Docker containers to host different games and make them playable from any local web browser.

__Done:__
- All static websites. ✔
- Static launcher game website, which links to all games. ✔
- NGINX Web Server support. ✔
- docker-compose.yml file written to run all containers at once. ✔

__Optional objectives (we're not doing these but just in case we have that much time'):__
- Add more games.
- Make docker-compose able to run in an Azure Container Instance.

# Instructions:
- Clone or download this repository to your PC.
- Install docker and docker-compose, you can find the official docker instructions here: https://docs.docker.com
- Open a Terminal in this directory (path/docker-project) and run:
```
$: docker-compose up
```
- This will download files, build images for the containers, and get them all running. Note: This could take a while the first time, depending on what docker images you already have downloaded in your computer and your internet speed. Next times will take considerably less.

While there's a game launcher website to redirect you to each game, you can also reach them by going to:
| Game | localhost: |
| ------------- | ------------- |
| Main website | 80  |
| Doom | 81  |
| Keen | 82  |
| Cosmo | 83  |
| Secret Agent | 84  |
| Prince of Persia | 85  |
| Infinite Mario Bros | 86  |
