# acme2k
![logo](https://raw.githubusercontent.com/karahobny/acmecolors/reorder/img/a.png)
### ACME INTERNATIONAL COMPILED EDITORS

#### THEY EDIT LIKE HELL.
```
   No editor made, pretty much anywhere,

surpasses our Acme in shape, material or finish.
```
solid forged of unsigned int pieces of best wrought C, linked at the binary; tag line is made of one piece of code, compiled with -funroll-loops to the the rest of the window column and warranted with a [permissive license](https://raw.githubusercontent.com/9fans/plan9port/master/LICENSE). text window has sufficient refactoring done to insure stability and prevent SEGFAULTing; has ug, but perfectly written shell: [rc](http://doc.cat-v.org/plan_9/4th_edition/papers/rc); acme is linted and debugged by a special compiler so that there are no functions that return structures or integer and floating numbers in object code not converted to known formats and byte orders; [config.h](https://github.com/karahobny/acmecolors/blob/master/acme/config.h) should be perfectly tempered by the user or it will fuck up. mkfiles are straight and true, so you will have no trouble on account of acme returning cryptic compiler errors and not compiling.

ready thyself for thine bodieth utmost horrrifiength challengeth and read more about [acme](http://acme.cat-v.org/)

## acme2k features

![a1](https://raw.githubusercontent.com/karahobny/acmecolors/reorder/img/a1.png)
>*who needs syntax highlighting when this fine piece of work purrs and shows that these fangs got all kinds of shades of visceral strewn around, yet in finite enough of quantities to forbid you from not appreciating its scarcity, elevating it from a mere editor to a sublime Rothko, while emacs sinks in it's kitschy aesthetics, no matter how hard the themes try to salvage that bloated-out-of-proportions Titanic...*

+ autoindent, swapscrollbars, fonts and colors configurable from config.h.

+ arrow keys navigate through text up one letter and down one letter instead of scrolling.

+ `ctrl+c`, `ctrl+x`, `ctrl+v` for snarfing, cutting and pasting selected text; `ctrl+z` for undo and `ctrl+r` for redo.

+ `home` and `end` move the cursor to the start or to the end of the current line respectively.

+ `delete` deletes all text from the start of the line until cursor position. (a placeholder feature really)

+ the end ... ?

# brass tacks (the serious business)
## dependencies
**acme2k** depends on `plan9port` which can be found [here on github](https://github.com/9fans/plan9port) or on your local repository. i know debian has stripped plan9 userpace called `9base` but i wouldn't roll my dice with this working wth it. don't know haven't a clue, now's yer chance to feel useful and test it out.

## installation
after following the instructions in your `$PLAN9`-folder to run `./INSTALL` and `mk`'ing every goddamn plan9 userspace application there happens to be ported, you can move right on to mangle it with this godawfulness:

![a2](https://raw.githubusercontent.com/karahobny/acmecolors/reorder/img/a2.png)
>*that low contrast base16-ocean just promises peace, quiet and solitude to your zen-like coding session. there's really no place like home, no place like home, no place like home*

just copy `acme`-folder to your `$PLAN9/src/cmd` replacing the existing `acme`-folder. ie.:

```bash
      cp -r acme $PLAN9/src/cmd/
```

you may need to build from the `INSTALL`-file located in the `$PLAN9`-root, but usually its enough to build from

```bash
      cd $PLAN9/src/cmd/acme; mk install
```

### config.h
`config.h` includes all the neccesary color and font modifications you just need to `mk install` it after every time you modify it, suckless style. 

#### fonts
`fontsrv -p .` to list all the available fonts and then use them like 
```bash
"/mnt/font/[listed font]/[font size][a(ntialias)/no a(antialias)]/font",
"/mnt/font/Monaco/9a/font",
"/mnt/font/GohuFont/9/font",
```
![a3](https://raw.githubusercontent.com/karahobny/acmecolors/reorder/img/a3.png)
>*dont be shackled by dark hues and saturated pinks, make Glenda, the Bunny, proud by showing off the team colors aka the Rio Windowing Systems. "little black-on-white makes a little rob pike smile. when? every now and then!", or so ive been told.*

in this case the first option would stand for Monaco size 9 antialised, the second for GohuFont size 9 aliased, ofc.

insert two fonts into config.h. the first one is treated as a proportional width font and is used everywhere by default. the second one can be activated for a specific window by executing `Font` from its tag window.

#### colors
colors need to be in the format of `0x*rgb hex color code*FF` without the prefixed hashtag. i'd suggest just to experiment what all the #defines mean but to start you with something `c_tagbg` means tag window background color. `c_txtbg` means text window backgorund color. `...hlbg/fg` means highlighted text background and foreground color etc. i've taken the liberty to comment all the color variations and what they affect on [config.h's noticeable comment section](https://github.com/karahobny/acme2k/blob/reorder/acme/config.h). go ahead and take a peek.

## but WHAT can I do
definetly check out [TODO](https://github.com/karahobny/acmecolors/blob/reorder/TODO.md) and feel free to chime in what would you like to see as a feature, add an issue or clone the repo and edit [TODO.md](https://github.com/karahobny/acmecolors/blob/reorder/TODO.md) and push it to the upstream, if all you want to do is add feature ideas. for bug fixes and coding features its better to contact me at:
````
karahobny at gmail dot com
````
or branch and send a pull request so i can check it out, dont worry ill always tip and youll get your name on the contributors list and you can for all i care, add your name on a comment preceding the codeblock in question, you know p. much what ever that doesnt harm the readability of the code, im all about you people having the respect you deserve for having partaken in such a sweet project.

## license (or whats the other one ive never heard of)
yeah no one's really heard of that other one, it was just a fucked up situation where plan9 guys' hands were forced by lawyers to use that for some reason. plan 9 also got gpl'd for some time but that version is meaningless and a joke afaik; up still here in github if it somehow jollies your gollies tho.

project is licensed (if ive understood correctly and this is possible), the original unmodified `plan9port/acme` being [**lucent public license**](https://github.com/karahobny/acme2k/blob/reorder/LICENSE.LUCENT) which specifically disallows any warranty, like every goddamn license in the whole goddamn universe and allows for me to sublicense it as i see fit so ive licensed specifically my modifications under [**mit license**](https://github.com/karahobny/acme2k/blob/reorder/LICENSE.MIT), simply because it's more straightforward a permissive license and nobody really has to second guess what its trying to allow/disallow me to do.

ive yet to have had to think about accepting contributions from other licenses than **lucent** or **mit** since this is still in its faltering baby steps, but id still hope if you would think about trying to avoid having a deck of licenses to show instead of like actual features in our repository. just think about it: **mit** stands for umm mankind institute of technology so you know thats smart, why would a license called something that smart be dumb, hm? riddle me that, atheists.



