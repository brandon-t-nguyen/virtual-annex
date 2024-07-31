# virtual-annex
## A git-annex helper

This is a tool to make symlinks to copies of files on more "preferred" storage locations (i.e. faster) so you don't have
to reconfigure software to point to different locations as they move around: all it takes is running this script to pick
out the preferred source of the file.
This is done through a file that lists each remote in order of preferrence. Planned is a tool to benchmark the annexes
to generating this ranking file.

Currently running this script requires you to refer to a "master" annex which is assumed to be on the fastest storage
available and thus has the highest precedence when linking files, and creates symlinks in another directory you specify.

The next iteration of this is to have it work with a separate, gateway repository (to borrow the term from clusters).
This repository will be a node that has each other annex as a remote, keeps in sync with them to keep up to date with
new files, and then apply its links on a separate branch.

TODO: refinements, documentation
