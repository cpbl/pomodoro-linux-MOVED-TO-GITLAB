# pomodoro-linux
 This is a simple, customisable "Pomodoro Method" or "Tomato method" timer for facilitating high-focus work.   It turns off your music and network for work periods, traditionally for 25 minutes at a time, and suggests a five minute break in between the work sessions.  Completed sessions are logged in a flexible, text-based log so you can do whatever you want (or nothing) with them. Whenever you finish a pomodoro, you can list any relevant tags to describe your work.   It runs some custom command line strings at the beginning and end of each tomato, for instance to block access to certain websites by interfering with /etc/hosts.  With the current settings, these sites are only unblocked at the end of the tomato, if the time is not during the 09h-17h workday (I work weekends :) )   It also works with one of a couple of music players on GNU/Linux so that any music that's playing when you start is paused and continues after you've logged your session.
 Lastly, you can "analyze" your log of work and generate a word cloud of your tags, or a plot of your logged minutes over time.
 
See wiki for screenshots.


```
$ pomodoro -h
Usage:
  pomodoro [options] [<minutes>]
  pomodoro [options] analyse 
  pomodoro [options] analyze

Options:
  -h --help                      Show this screen.
  -n --with-network              Use this to keep the network active during the tomato
  --player=<musicplayer>         Set this to banshee or rythmbox to pause music (or leave it to try both)
  -l LOGFILE --logfile=LOGFILE   TSV file to store list of tomato sessions 
                                   [default: ~/.pomodoro-log.txt]
  -e EDITOR --editor=EDITOR      Editor to use for reporting tags [default: emacs]
```

