# prompt

## How to use

Copy the `prompt` file somewhere on your computer, e.g. `/usr/local/bin/prompt`
or `~/bin/prompt`, make sure it is executable, and add the following to your
`~/.profile`:

```sh
# Prompt setup
export PROMPT_COMMAND="/usr/local/bin/prompt -c \$COLUMNS; $PROMPT_COMMAND"
export PS1='\u@\h\$ '
```
