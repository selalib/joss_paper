# SeLaLib joss paper


[![PDF](https://github.com/selalib/joss_paper/workflows/Paper\ Draft/badge.svg)](https://github.com/selalib/joss_paper/actions)

Build the pdf with:

```bash
docker run --rm --volume $PWD:/data \
    --user $(id -u):$(id -g) --env JOURNAL=joss openjournals/paperdraft
```
