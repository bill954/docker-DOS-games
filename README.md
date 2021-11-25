# docker-project

<img src="https://www.docker.com/sites/default/files/d8/styles/role_icon/public/2019-07/Moby-logo.png?itok=sYH_JEaJ" width="250px">

The current objective of this project is to use Docker containers to host different games and make them playable from any local web browser.

__Done:__
- All static websites. ✔
- Static launcher game website, which links to all games. ✔
- NGINX Web Server support. ✔
- docker-compose.yml file written to run all containers at once. ✔
- You can now host containers so others can access them online. ✔

__Optional objectives (currently not working on these but maybe someday):__
- Add more games.
- Make docker-compose able to run in an Azure Container Instance.
- Make html mobile friendly.

# Instructions:
- Clone or download this repository to your PC.
- Install docker and docker-compose, you can find the official docker instructions here: https://docs.docker.com
- Open a Terminal in the main directory of this repo and run:
```
$: docker-compose up -d
```
- This will download files, build images for the containers, and get them all running. Note: This could take a while the first time, depending on what docker images you already have downloaded in your computer and your internet speed. Next times will take considerably less.

- To stop all the containers at once, while on the same directory, run:
```
$: docker-compose down
```

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

# Do you want to host the containers to let others play on them?
- You need to open the ports 80 to 86 on your route and redirect them to the ports 80 to 86 in your PC. Since this must be done differently in every router, you will have to search for instructions that apply to yours especifically.
- You also need your public IP address. You can do that here: https://www.whatismyip.com/what-is-my-public-ip-address/
- Now, you need to open a terminal in the main directory of this repository and run this command:
```
$: sed -i 's/localhost/your_router_ip/g' docker-games/web_server/debian-nginx-11.21.4/html/index.html
```
- And that's it! Next time you run ```docker-compose up``` you can access the games by going to your public IP on a browser on any other PC.
