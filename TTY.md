# TTY using bash

During an attack phase, when we manage to get a reverse shell given a victim IP during a pentesting, there comes a time when we have to connect to the victim machine to be able to rummage through the internal files or even manage to escalate its privileges. It is at that moment when we have to do a treatment to the tty.

## Instructions on Bash:
Check that we have the connection established. Running the *whoami* command should return the hostname.
```bash
whoami
script /dev/null -c bash
ctrl + z
stty raw -echo; fg
reset
export TERM=xterm // export SHELL=bash
stty rows 40 columns 123
```
## Using python
```bash
python3 -c 'import pty;pty.spawn("/bin/bash")'
export TERM=xterm
ctrl + z
stty raw -echo; fg
```
