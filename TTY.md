# TTY using bash

```bash
whoami
script /dev/null -c bash
[CTRL + Z]
stty raw -echo; fg
reset xterm
export TERM=xterm
export SHELL=bash
stty rows 51 columns 189
reset xterm
```

# TTY using Python

```python
which python
python -c 'import pty;pty.spawn("/bin/bash")'
[CTRL + Z]
stty raw -echo; fg
reset xterm
export TERM=xterm
export SHELL=bash
stty rows 51 columns 189
```
