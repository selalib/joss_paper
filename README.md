# SeLaLib joss paper


[![draft pdf](https://github.com/selalib/joss_paper/workflows/paper/badge.svg)](https://github.com/selalib/joss_paper/actions)

Build the pdf with:

```bash
docker run --rm --volume $PWD:/data \
    --user $(id -u):$(id -g) --env JOURNAL=joss openjournals/paperdraft
```
