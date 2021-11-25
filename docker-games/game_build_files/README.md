# Dockerized DOS games.
- This applies to all the games in this folder except Infinite Mario Bros

Each `.Dockerfile` uses a `wget` command to download a compressed `.zip` file that holds a game from the web.
If you want to run a different game, not available here:
- Copy any of these folders and rename as 'any_game_of_your_choice' (the name of the folder does not affect)
- Go to the `.Dockerfile` inside your new folder and change these two lines:
	- ENV GAME_URL="(paste the download link to the .zip file of the game you want to play)"
	- ENV GAME_ARGS=\"(path to the executable file of the game inside the .zip)\"
