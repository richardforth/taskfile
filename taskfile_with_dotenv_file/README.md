```bash
$ task --init
Taskfile created: Taskfile.yml
$ vim Taskfile.yml 
$ task hello
Endpoint is: testing123.com
```

I disallow committing .env files to GitHub, but it contains the following (non-sensitive) value:

```bash
ENDPOINT=testing123.com
```
