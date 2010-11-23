# Git-Pivotal
by [Jason Ardell](http://github.com/ardell)

A git subcommand used to query Pivotal Tracker.  So you don't have to have a Pivotal window open all day.

## Usage:
    []:> git pivotal list
    === Iteration: current (1 of 1) ===
    [1234567] Some task that I'm currently working on                 started

    === Iteration: backlog (2 of 12) ===
    [1234568] Foo bar #1                                            unstarted
    [1234569] Foo bar #2                                            unstarted

    []:> git pivotal list current
    === Iteration: current (1 of 1) ===
    [1234567] Some task that I'm currently working on                 started

    []:> git pivotal show 1234567
    [1234567] Some task that I'm currently working on                 started
    Description: This is a task that I'm currently working on.

    []:> git pivotal start 1234568
    [1234568] Foo bar #1

    Enter a name for your branch: [fooBar1]
    Checking out branch: fooBar1-1234568-yourname
    Switched to a new branch 'fooBar1-1234568-yourname'

## Commands

### List
Lists all the stories assigned to you from 'current' and 'backlog' iterations.

List is the default command of git pivotal, so 'git pivotal' is equivalent to 'git pivotal list'.  Use 'git pivotal list [iteration]' to only show stories from current or backlog iterations.

### Show
Shows the details of a particular story, including story id, name, current state (unstarted, started, etc), and description.

### Start
Start a particular story.  Marks the story as 'started' in pivotal and checks out a branch entitled [prefix]-[branchName]-[storyid]-[yourname] in git.  Git pivotal will prompt for a branchName [a-zA-Z0-9\-].

## Installation:
1. git-clone this project
2. Symlink git-pivotal into /usr/bin (ln -s /full/path/to/git-pivotal /usr/bin/git-pivotal)

## Requirements:
PHP 5+

## License
MIT.

## Todo
* Allow filtering the list command, e.g. by author, status, etc.
* Show backlog tasks in order as scheduled.
* Show/manage tasks
* Show notes
* Add more details to git pivotal show?