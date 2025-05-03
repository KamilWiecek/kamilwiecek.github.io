# How tu build and run it

```bash
export JEKYLL_VERSION=4.2.2
docker run --rm  --volume="$PWD:/srv/jekyll:Z" -it jekyll jekyll:$JEKYLL_VERSION  jekyll build
```

```bash
export JEKYLL_VERSION=4.2.2
docker run --rm \
  --volume="$PWD:/srv/jekyll:Z" \
  --publish [::1]:4000:4000 \
  jekyll/jekyll:$JEKYLL_VERSION \
  jekyll serve
```