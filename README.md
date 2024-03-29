## SSH Toolkit ##

I use ssh a lot. To make life a little easier, I've cobbled together a few things:


### openssh wrappers ###

These are bash-script wrappers around the ssh command.

* `lssh`

To get session logs, `lssh` invokes `script` to capture ssh sessions to a directory with each one named `YYYY-MM-DD-MyHostname-Remotehostname.log`. 

* `tssh`

`tssh` does the same thing only it wraps `lssh` in a tmux session with the short hostname as the tmux pane label. See my [dotfiles](https://github.com/V01dDweller/dotfiles) repo for my tmux config. Both wrappers can optionionally apply mintty (MinTTY/WSLTTY, GitBash) color schemes.

### ssh log reading ###

I find that I frequently need to remember what I did on a collection of hosts on a certain day. These scripts allow me to create "daily" reports based on the logging collected by the lssh or tssh. The "search" scripts try to pinch out only that command issued, minus output, so I can get an idea of what I was working on. The scripts are just looking for my go-to bash prompt which can be found in my .bash_profile or .bashrc in the dotfile repo.

* `daily` - Shows log report for spcified date, usage, e.g.: `daily 2018-06-08`
* `daily2` - Same as above only it shows the custom prompt with the command, e.g. to see the time stamps, etc.
* `search` - attempts to pinch just the commands issued from the log, e.g. `search <log-file-name>`
* `search2`
* `search3`
* `search4`
