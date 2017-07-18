## SSH Toolkit ##

I spend all day logging into Linux servers via ssh. My favorite ssh client is the Cygwin openssh-client (yes, I'm an unrepetant Windows user) via Mintty. To make life a little easier.


### openssh wrappers ###

These are wrappers around the ssh command. To get session logging, lssh invokes script to capture each session to a directory with each session file using YYYY-MM-DD-MyHostname-Remotehostname.log. tssh does the same thing only it wraps lssh in a tmux session, complete with tmux labels. See my "dotfiles" repo for my tmux config. Both wrappers can optionionally apply mintty color schemes. 

* lssh
* tssh

### ssh log reading ###

I find that I freqently need to remember what I did on a collection of hosts on a certain day. These scripts allow me to create "daily" reports based on the logging collected by the lssh or tssh. The "search" scripts try to pinch out only that commands issued in each session, while skipping whatever output followed, so I can get an idea of what I was doing at the time without too much clutter. The scripts are looking for my go-to bash prompt which can be found in my .bash_profile or .bashrc in the dotfile repo.

* daily
* daily2
* README.md
* search
* search2
* search3
* search4
