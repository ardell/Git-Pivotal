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

## Installation:
1. git-clone this project
2. Symlink git-pivotal into /usr/bin (ln -s /full/path/to/git-pivotal /usr/bin/git-pivotal)

## Requirements:
PHP 5+

## License
MIT.