```bash
$ mkdir task_init
$ cd task_init/
$ task --init
Taskfile created: Taskfile.yml
$ cat Taskfile.yml 
# https://taskfile.dev

version: '3'

vars:
  GREETING: Hello, World!

tasks:
  default:
    cmds:
      - echo "{{.GREETING}}"
    silent: true
$ task
Hello, World!
$ 
```

Note: Because we have a task called `default`, simply running `task` without specifying a named task is fine, if you don't have a `default` task, you will get an error like the below, with a helpful hint:

(Note the below was taken from the hello_world folder)

```bash
$ task                                                                                                                                            
task: No tasks with description available. Try --list-all to list all tasks                                                                                
task: Task "default" does not exist                                                                                                                        
$ task --list-all                                                                                                                                 
task: Available tasks for this project:                                                                                                                    
* hello: 
```

In the `hello_world` folder, you can see that the error appeared, suggesting to us to run `task --list-all`, which then allowed us to run `task hello` (not shown).
