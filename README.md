# prompt

## What for

`prompt` will allow you to display the full path of your working directory
on a separate line, just above the shell’s prompt. This mean you can have a
short prompt, while having the working directory printed.

If there is enough place, `prompt` will also display the current date after the
working directory.

If there is not enough place to display the working directory on one line,
`prompt` will only display the end of it.

![Screenshot](/Screenshot.png)

## How to use

Copy the `prompt` file somewhere on your computer, e.g. `/usr/local/bin/prompt`
or `~/bin/prompt`, make sure it is executable, and add the following to your
`~/.profile`:

```sh
# Prompt setup
export PROMPT_COMMAND="/usr/local/bin/prompt -c \$COLUMNS; $PROMPT_COMMAND"
export PS1='\u@\h\$ '
```
