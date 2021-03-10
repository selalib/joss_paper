# joss_paper

Build the pdf with:

```bash
docker run --rm --volume $PWD:/data \
    --user $(id -u):$(id -g) --env JOURNAL=joss openjournals/paperdraft
```
