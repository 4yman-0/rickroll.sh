# rickroll.sh
BASH script which [rickrolls](http://en.wikipedia.org/wiki/Rickrolling) the terminal by
playing Rick Astley’s “Never Gonna Give You Up” with ANSI 256-color coded UTF-8
characters and audio (if available).

## How to Roll
To start rickrollin’ immediately:

```bash
curl -sL https://raw.githubusercontent.com/4yman-0/rickroll.sh/main/roll | bash
```

Here is the clandestine command you can give to your friends 😈

```bash
curl -sL https://bit.ly/3zvELNz | bash
```

>For the record: It is not a good idea to make a habit of
>
>```bash
>curl $(random_script_from_the_internets) | bash"
>```

Nevertheless, for the enhanced experience, I highly recommend the following:

```bash
wget https://raw.githubusercontent.com/4yman-0/rickroll.sh/main/roll
chmod +x roll

./roll inject
```

Which essentially just does:

```bash
echo "curl -s -L http://bit.ly/10hA8iC | bash" >> ~/.bashrc
```

>For a salutary lesson in the importance of taking care what you
execute in your terminal, inspired by the classic
<a href="https://github.com/mtoyoda/sl"><code>sl</code></a> , save the
command in a shell script somewhere on your `PATH`. It’s
recommended to download the script for faster startup, to avoid
spoiling the surprise when you accidentally execute it for the `n`th
time (and also, unless you really like living dangerously, for
security, in case we are possessed to replace `roll`
with something evil).

## Misc.
>This has been tested on Arch, Debian, Ubuntu, Mac and Cygwin (so far).
To enable sound in Cygwin, install the **sox** package.

Since this is a colorful hobby, you need to ensure 256-color mode is enabled or
Astley will look sad.

>For example, if you use GNU screen, ensure your ~/.screenrc contains something
>like:
>```bash
>termcapinfo xterm 'Co#256:AB=\E[48;5;%dm:AF=\E[38;5;%dm'
>defbce "on"
>```

>Kudos to jart for our lovely hiptext shenanigans.
>Please see our sister project: [hiptext](https://github.com/jart/hiptext), which
>generates ANSI color codes for any image or video.
>
> ~ serene ([@kiserene](http://twitter.com/kiserene))
