# Dockerized DOS games.
- This applies to all the games in this folder except _Infinite Mario Bros_ and _Prince of Persia_.

Each dockerfile for each game uses a `wget` command to download a compressed .zip file game from the web.
If you want to run a game not available here:
- Copy any of these folders and rename as 'any_game_of_your_choice' (the name of the folder does not affect)
- Go to the dockerfile inside your new folder and change these two lines:
	- ENV GAME_URL="(paste the download link to the .zip file of the game you want to play)"
	- ENV ENV GAME_ARGS=\"(executable_file_of_the_game.zip)\"

- The dockerfile of _Prince of Persia_ is a bit different. It uses a .zip that is already downloaded. To load another DOS game this way:
    - Download the .zip file
    - Copy the _Prince of Persia_ folder and rename it.
    - Copy your downloaded .zip into this folder.
    - Modify these lines of the Dockerfile:
        - COPY ./name_of_your_compressed_folder.zip game.zip
        - ENV GAME_ARGS=\"(executable_file_of_the_game.zip)\"

- **Note:** The _Infinite Mario Bros_ game doesn't need any compressed .zip file to be downloaded and decompressed to run.

# Credits
- The original idea and code to create these containers came from: https://earthly.dev/blog/dos-gaming-in-docker/ (except the Mario game).
- The Mario game was obtained from: https://github.com/PengBAI/mariohtml5
