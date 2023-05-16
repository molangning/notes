Firstly, spawn pty terminal with python:

`python3 -c 'import pty;pty.spawn("/bin/bash");'`

If python3 does not exist, try this instead:

`python -c 'import pty;pty.spawn("/bin/bash");'`

Afterwards, type the following commands to change terminal type to xterm:
`export TERM=xterm`

Now press ctrl+Z to suspend the reverse shell and type in the following:

`stty raw -echo;fg`

The above command prevents the terminal from echoing back the typed in text
and resumes the suspended reverse shell

Simple copy and paste:
```
python3 -c 'import pty;pty.spawn("/bin/bash");'
export TERM=xterm
```
ctrl+z

`stty raw -echo;fg`