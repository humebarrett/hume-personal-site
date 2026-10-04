# Hume — personal site

A personal page about Hume’s working style, likes, dislikes, and lessons learned. It includes a locally hosted photo gallery and runs on nginx in Docker.

## Build and run

```sh
docker build -t hume-personal-site .
docker run --rm -p 8080:80 hume-personal-site
```

Then open http://localhost:8080. The gallery images are stored in `assets/`, so the site does not depend on an external image host.

The page includes an original illustrated avatar and three locally hosted Unsplash photographs: a coding desk, a laptop with code and notebook, and a road through red-rock country. Images are bundled in `assets/`; the site does not rely on an external image host. See https://unsplash.com/license.

To publish it, tag the image with a registry path and push it after logging in:

```sh
docker tag hume-personal-site ghcr.io/YOUR-ACCOUNT/hume-personal-site:latest
docker push ghcr.io/YOUR-ACCOUNT/hume-personal-site:latest
```
