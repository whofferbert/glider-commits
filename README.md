# glider-commits


```bash


  Draw a glider on your git activity chart.

  This script schedules git commits to be executed with the 'at' daemon
  at specific times to draw a glider on the activity chart.

  To prevent accidental commits wrecking the image, an alias is temporarily 
  added to your ~/.bashrc to provide a warning message instead of calling 
  the actual 'git'.

  To circumvent this behavior, specify the complete path to git (/usr/bin/git)

Usage

  glider-commits [options] [--engage|--disengage]

Options:

  --engage | -E
    Engage the mechanism. This disables your 'git' shortcut and
    plots to commit changes at specific times to draw the glider

  --disengage | -D
    Disengage the mechanism. Puts your ~/.bashrc back to the way it was
    It should probably remove the any remaining at jobs too, but it doesn't

  --offset-hours | -O   [INTEGER]
    Specify an integer number of hours to offset the commits by
    Default is 6

  --repitition | -r   [INTEGER]
    Specify the minimum number of commits to make each day
    Default is 6

  --delay-secs | -d   [INTEGER]
    Specify the number of seconds to wait between repeated commits
    Default is 60

  --help | -h
    Display this help text.



```
