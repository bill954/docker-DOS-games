FROM node:16.3.0-alpine

WORKDIR site

RUN wget https://js-dos.com/6.22/current/js-dos.js && \
    wget https://js-dos.com/6.22/current/wdosbox.js && \
    wget https://js-dos.com/6.22/current/wdosbox.wasm.js

RUN npm install -g serve

ENV GAME_URL=https://image.dosgamesarchive.com/games/keen-shr.zip
RUN wget -O game.zip $GAME_URL

ENV GAME_ARGS=\"KEEN.BAT\"
COPY html/index.html .
RUN sed -i s/GAME_ARGS/$GAME_ARGS/ index.html

ENTRYPOINT npx serve -l tcp://0.0.0.0:8000
