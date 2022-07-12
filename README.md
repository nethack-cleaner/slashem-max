This file contains installation instructions; the part below has been written by MetaNite64, NOT by Amy, which means that I (Amy) take no responsibility if it doesn't work as advertised :D Also, it's mainly for installing SLEX on unix-like systems. If you're playing on Windows, your best bet would be to download PuTTY and connect to slashem@slashem.me (em.slashem.me with password slashem), port 22, connection type ssh. But if you want to play locally on Windows, get the precompiled binary from either Github or https://app.box.com/s/bjmryzddy3t7llv6jekb or compile it yourself with e.g. MinGW (look for the SLASH'EM Extended page on Nethackwiki for instructions on how to do that; you should look at that page anyway if you're a new player because it has a list of hints, tips and tricks on how to play).

------ (MetaNite64's install readme begins below) -------

# SLASH'EM Extended
## The Basics
First off, I would like to let you know that SLASH'EM Extended (SLEX) is not for those who do not regularly use the terminal. You should have basic knowledge of how to use VI or have access to a number pad. You also should be able to use a package manager, and SSH.

## How To Install

### Local Installation
If you don't or won't have internet, you will have to install it locally. You should first have `git`, `ncurses`, `bison`, `flex`, and `make` to be able to install it. With `apt`, you'll need to run `sudo apt install libncurses5-dev bison flex make git`. On Fedora/with `dnf`, you should run `sudo dnf install ncurses-devel bison flex git`. With `pkg`, you should run `sudo pkg install ncurses bison flex gmake git`. You get the point.
From there, you should run `git clone [repo name]`. You'll then want to `cd` into the new directory `SLASH'MAX`, and run `sh sys/unix/setup.sh`. Finally, run `make -f sys/unix/GNUmakefile && make -f sys/unix/GNUmakefile install`. Go back to your home directory, and you'll want to run `cd maxslash/maxslash-2.8.0`, and then `./maxslash`.

[Amy edit: the game has two main control schemes, which are number pad and vikeys. On most Unix installs, the number pad is off by default so you have to use hjklyubn keys to move around, while on Windows installs the number pad is usually on by default. If you try to use an invalid command within the first 50 game turns, there will be a prompt asking whether you want to change the number pad setting; you should *read the message of that prompt* (yes, really, don't just skip past it; in fact, you generally shouldn't skip past messages while playing this game unless you want to die out of the blue) and act accordingly - the prompt tells you exactly what to do in order to switch between number pad and vikeys mode. This also applies if you find the prompt annoying, because it mentions how you can turn it off if it's getting on your nerves. You should also edit your config file accordingly, the following lines can be helpful:
OPTIONS=number_pad:0 - this turns the number pad off, i.e. enables vikeys
OPTIONS=number_pad:2 - this turns the number pad on
OPTIONS=nonumpadmessage - this turns the "Do you want to turn on/off the number pad?" prompt off
Have fun!]
