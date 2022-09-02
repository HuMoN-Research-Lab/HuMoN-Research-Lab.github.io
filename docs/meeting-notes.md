# 2022-09-02 -  FreeMoCap Pair Programming 

[![hackmd-github-sync-badge](https://hackmd.io/OoHK-ZoRTXS27lC_xS2JVw/badge)](https://hackmd.io/OoHK-ZoRTXS27lC_xS2JVw)

The plan for this meeting is that Jon will guide Aaron through the process of fixing some of the bugs that popped up when testing out the freemocap GUI

###### tags: `freemocap`, `pycharm`, `python`

- Aaron has UX notes
- mainly want to target breaking bugs
    - output folder getting the wrong name
    - blender exe path not being hard coded
- also want to use this as opportunity to talk abot how to navigate this code base (specifically via PyCharm because thats what I've been using )

## Reference - pycharm shortcuts that I rely on a lot

### shift-shift
locate a 'pattern' within the code base, i.e. I can remember the name of the variable but where is it? 

### ctrl-shift-F 
Same thing but also search strings and file paths and stuff

### crtl-B
tells you where a function/class/method is called elsehwere in the program

super helpful for following work paths and whatnot

### alt-enter

Suggested fixes for thigns (including `auto-import`). This is really essential because we're using the model of many many small files

e.g. you can define a function in a file, and then call it whereever you need to use it, it will show an error (red underline) and then you can hit it with `alt-enter` and it will offer to auto-import that function into this file 

### ctr-alt-s

pycharm settings

### ctrl-F6

'refactor' the name of a variable (so you can change it in one place and it automatically update the names elsewhere)

### ctrl-alt-L

auto-format the python script (to align with PEP-8 standards, I think)