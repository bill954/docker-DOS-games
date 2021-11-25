# Dockerized DOS games.
- This applies to all the games in this folder except Mario and Prince of Persia.

Each dockerfile for each game uses a wget command to download a .zipped game from the web.
If you want to run another game:
- Copy any of these folders and rename as 'any_game_of_your_choice' (the name of the folder does not affect)
- Go to the dockerfile inside your new folder and change these two lines:
	- ENV GAME_URL="(paste the download link to the .zip file of the game you want to play)"
	- ENV ENV GAME_ARGS=\"(executable_file_of_the_game.zip)\"

- The Dockerfile of Prince of Persia is a bit different. It uses a .zip that is already downloaded. To load another DOS game this way:
    - Download the .zip file
    - Copy the prince folder and rename it.
    - Copy your downloaded .zip into this folder.
    - Modify these lines of the Dockerfile:
        - COPY ./name_of_your_compressed_folder.zip game.zip
        - ENV GAME_ARGS=\"(executable_file_of_the_game.zip)\"

# Credits

The original idea and code to create these containers came from: https://earthly.dev/blog/dos-gaming-in-docker/ (except the Mario game).
The Mario game was obtained from: https://github.com/PengBAI/mariohtml5
