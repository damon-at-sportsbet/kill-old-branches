# kill-old-branches

OSX Only! (see below)

*Disclaimer:* This is a dangerous tool that deletes branches from your remote git repo!
Sportsbet is not liable for any loss of code or other property that this tool causes.

## description

a simple bash script that deletes all git branches in a project older than X days old that have 
already been merged to the master branch.

if you really want to use it, the actual delete command has been wrapped in an echo statement.
Remove the echo and the quotes to make it work.

## Usage
- copy the script file from this project into your executable path somewhere
- cd into your project folder base
- run `git fetch -p` to do a fetch and remove already deleted remote branches
- run `kill-old-branches list` to see which branches it would delete
- then, if you're really really absolutely certain, run: `kill-old-branches do-it`
to actually push those deletes to remote origin.

## Why OSX only?
it's only the format of the date command in the script that is BSD style, if you want to change
that it should work fine in linux.
