# SLASH'MAX

SlASH'MAX principle:  This is a direct port of version 2.7.7 with all of the words I was concerned about removed completely and removal of about 12 of the types of nasty traps that I thought were too much of an "interface screw".

So there is still a lot left and there are still 200+ nasty traps available, but the ones that are super bad aren't there.

## How To Install

1. You should first have `git`, `ncurses`, `bison`, `flex`, and `make` to be able to install it.
- With `apt`, you'll need to run `sudo apt install libncurses5-dev bison flex make git`. On Fedora/with `dnf`, you should run `sudo dnf install ncurses-devel bison flex git`. With `pkg`, you should run `sudo pkg install ncurses bison flex gmake git`. You get the point.

2. From there, you should run `git clone [repo name]`.

3. You'll then want to `cd` into the new directory and run `sh sys/unix/setup.sh`.

4. Then run `make -f sys/unix/GNUmakefile && make -f sys/unix/GNUmakefile install`.

5. Go back to your home directory, and you'll want to run `cd maxslash/maxslash-2.8.0`, and then `./maxslash`.
