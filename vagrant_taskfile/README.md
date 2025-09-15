# Important

It turns out that this Taskfile didnt do exactly what I wanted, and I found out that each cmd entry runs in its own little subshell. What this means in practice is, you end up back in your home directory after the Taskfile completes, hence the final echo, just in case you thought that was a bit wierd.

## All the automation runs fine

You just have to remember that it will run in subshells and not actually switch you into the directory you think it should at the end of it all.

## Added a description: makes `--list-all` much easier to understand with an appropriate description

```bash
vagrant@vagrant:~$ task --list-all
task: Available tasks for this project:
* default:       do the needful with git fetch/pull in working dir /vagrant/git/taskfile
```
