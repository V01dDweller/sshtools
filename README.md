## SSH Toolkit ##

I spend all day logging into Linux servers via ssh. My favorite ssh client is the Cygwin openssh-client (yes, I'm an unrepetant Windows user) via Mintty. To make life a little easier.


### openssh wrappers ###

These are wrappers around the ssh command. The get session logging, lssh invokes script to capture each session to a directory with each session file using YYYY-MM-DD-MyHostname-Remotehostname.log. tssh does the same thing only it wraps lssh in a tmux session, complete with tmux labels. See my "dotfiles" repo for my tmux config. Both wrappers can optionionally apply mintty color schemes. 

* lssh
* tssh
* daily
* daily2
* README.md
* search
* search2
* search3
* search4
