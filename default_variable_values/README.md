```bash
$ task --init
Taskfile created: Taskfile.yml
$ vim Taskfile.yml 
$ task msg
task: [msg] echo "Message is: Testing123"
Message is: Testing123
$ task msg MESSAGE=HelloWorld
task: [msg] echo "Message is: HelloWorld"
Message is: HelloWorld
```
