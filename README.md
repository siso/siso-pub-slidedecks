# siso's public slide-decks

## Slide-deck powered by Docker, node.js and reveal.js

Build Docker image:

```shell
docker build -t="siso/siso-revealjs" .
```

Launch Docker container from image:

```shell
docker run -p 8000:8000 --name "siso-pub-slidedecks" -v $(pwd)/slide-deck:/opt/reveal.js/slide-deck -d "siso/siso-revealjs"
```

View the presentation:

- http://127.0.0.1:8000/slide-deck#/
- http://BOOT2DOCKER-IP:8000/slide-deck, OS X users should replace `BOOT2DOCKER-IP` with `$(boot2docker ip)`

Start and stop Docker container:

```
$ docker start siso-pub-slidedecks
$ docker stop siso-pub-slidedecks
```

## Export as PDF

Point web browser to:

- http://localhost:8000/slide-deck/?print-pdf

Print, and select "save as PDF".

## Links

- [Presenting with Docker](http://kartar.net/2014/05/presenting-with-docker/) by James Turnbull

## TODO

- Fix speaker's notes
- Image is broken, http://0.0.0.0:8000/slide-deck/#/35/1
