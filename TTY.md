# TTY using bash

During an attack phase, when we manage to get a reverse shell given a victim IP during a pentesting, there comes a time when we have to connect to the victim machine to be able to rummage through the internal files or even manage to escalate its privileges. It is at that moment when we have to do a treatment to the tty.

## Instructions on Bash:
Check that we have the connection established. Running the *whoami* command should return the hostname.
```bash
whoami
```
Launch an interactive bash (a pseudo console).

```bash
script /dev/null -c bash
```
Send the process that is running to the background.

```bash
[CTRL + Z]
```
Resume the process previously left in the background (3)

```bash
stty raw -echo; fg
```
Restart the current configuration of the terminal (after this step we should be able to operate the external terminal more comfortably).

```bash
reset xterm
```
We export an Xterm terminal

```bash
export TERM=xterm
```
We export a bash

```bash
export SHELL=bash
```
Change the resolution of our interactive bash. Note: To check the number of current rows and columns run -> stty size.
```bash
stty rows 51 columns 189
```
Restart the current terminal configuration again.
```bash
reset xterm
```

## Instructions on Python:
Check if there is python installed (you shoud see an output)
```bash
which python
```
Spown the bash using python
```bash
python -c 'import pty;pty.spawn("/bin/bash")'
```
Send the process that is running to the background.

```bash
[CTRL + Z]
```
Resume the process previously left in the background (3)

```bash
stty raw -echo; fg
```
Restart the current configuration of the terminal (after this step we should be able to operate the external terminal more comfortably).

```bash
reset xterm
```
We export an Xterm terminal

```bash
export TERM=xterm
```
We export a bash

```bash
export SHELL=bash
```
Change the resolution of our interactive bash. Note: To check the number of current rows and columns run -> stty size.
```bash
stty rows 51 columns 189
```
Restart the current terminal configuration again.
```bash
reset xterm
```
