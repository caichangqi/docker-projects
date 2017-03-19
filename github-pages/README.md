## Create github pages images

```bash
docker build -t github-pages .
```

## Run github pages image

```bash
docker run --rm -p 4000:4000 -v /path/to/github-pages:/code github-pages bundler exec jekyll serve --host 0.0.0.0
```