# glider-commits


```bash

  Draw a glider on your git activity chart.

  This script schedules git commits to be executed with the 'at' daemon
  at specific times to draw a glider on the activity chart.

  To prevent accidental commits wrecking the image, an alias is temporarily 
  added to your ~/.bashrc to provide a warning message instead of calling 
  the actual 'git'.

  To circumvent this behavior, specify the complete path to git (/usr/bin/git)

  NOTE that if you use git from many computers, you run the risk of bypassing
  the ~/.bashrc change. 

  You will also have to re-source your ~/.bashrc or log out and back in to 
  have the changes take affect.


Usage

  glider-commits [options] [--engage|--disengage]

Options:

  --engage | -E
    Engage the mechanism. This disables your 'git' shortcut and
    plots to commit changes at specific times to draw the glider

  --disengage | -D
    Disengage the mechanism. Puts your ~/.bashrc back to the way it was
    and remove any reamining glider jobs from the atq

  --offset-hours | -O   [INTEGER]
    Specify an integer number of hours to offset the commits by
    Default is 6

  --repitition | -r   [INTEGER]
    Specify the minimum number of commits to make each day
    Default is 42

  --delay-secs | -d   [INTEGER]
    Specify the number of seconds to wait between repeated commits
    Default is 60

  --project-dir [/path/to/git/project]
    Specify the project to update
    Default is /home/whofferbert/git/bash/hacker-glider-commit

  --update-file [filename]
    Specify the file to overwrite with random data
    Default is dummy_file

  --rcfile [/path/to/rcfile]
    Specify an rcfile to adust instead of /home/whofferbert/.bashrc
    Must support bash-style functions and alias

  --git-push-string 'push string'
    Specify the push string to use for the git push
    Default is push -u whofferbert master

  --help | -h
    Display this help text.


Examples

  ./glider-commits --engage
  # Turn the mechanism on

  ./glider-commits --disengage
  # Turn the mechanism off




```
