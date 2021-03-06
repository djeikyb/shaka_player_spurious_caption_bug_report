# Shaka Player spurious caption bug

Reported as issue [google/shaka-player#3250](https://github.com/google/shaka-player/issues/3250)

## Versions affected

3.0.0 - 3.0.10. The example here uses shaka player 3.0.10

## Run this example

1. Host the files here in a web server. I used nginx in docker, like:

```
docker run --rm -p 8080:80 --name web -v "$PWD":/usr/share/nginx/html nginx:1.19
```

2. Open the page in macos safari, I used safari 14.0.3 (14610.4.3.1.7): http://localhost:8080

3. Look at the text tracks, there is a track labeled "Unrecognized ()". But you can see that no text tracks are configured. None in the hls playlist, none in the player config.

## What I see

![gif of bug; first click kebab control panel icon, then click captions, then see a text track labeled "Unrecognized ()"](spurious_caption.gif)
