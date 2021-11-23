# Dockerized DOS games.
- This applies to all the games in this folder except Mario

Each dockerfile for each game uses a wget command to download a .zipped game from the web.
If you want to run another game:
- Copy any of these folders and rename as 'any_game_of_your_choice' (the name of the folder does not affect)
- Go to the dockerfile inside your new folder and change these two lines:
	- ENV GAME_URL="(paste the download link to the .zip file of the game you want to play)"
	- ENV GAME_ARGS=\"(path to the executable file of the game inside the .zip)\"
