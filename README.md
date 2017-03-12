# prompt

## What for

`prompt` will allow you to display the full path of your working directory
on a separate line, just above the shell’s prompt. This mean you can have a
short prompt, while having the working directory printed.

If there is enough place, `prompt` will also display the current date after the
working directory.

<pre><span style="color: green;">~/a/typical/terminal/line/is/80/chars/long</span>         <span style="color: red;">Sunday March 12 2017 06:13:11</span>
etienne@axtar$
</pre>

If there is not enough place to display the working directory on one line,
`prompt` will only display the end of it.

<pre><span style="color: green;">...0/chars/long/this/is/a/very/very/long/path/so/that/it/does/not/fit/in/on/line</span>
etienne@axtar$
</pre>

## How to use

Copy the `prompt` file somewhere on your computer, e.g. `/usr/local/bin/prompt`
or `~/bin/prompt`, make sure it is executable, and add the following to your
`~/.profile`:

```sh
# Prompt setup
export PROMPT_COMMAND="/usr/local/bin/prompt -c \$COLUMNS; $PROMPT_COMMAND"
export PS1='\u@\h\$ '
```
