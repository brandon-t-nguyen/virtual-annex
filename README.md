# virtual-annex
## A git-annex helper

This is a tool to make symlinks to copies of files on more "preferred" storage locations (i.e. faster) so you don't have
to reconfigure software to point to different locations as they move around: all it takes is running this script to pick
out the preferred source of the file.
This is done through a file that lists each remote in order of preferrence. Planned is a tool to benchmark the annexes
to generating this ranking file.

This uses a separate repository to act as a sort of switchboard to find the files, co-opting Git's and git-annex's
infrastructure. This also has an simple I/O benchmark to sort remotes.
This repository will be a node that has each other annex as a remote, keeps in sync with them to keep up to date with
new files, and then apply its links on a separate branch.

TODO: refinements, documentation
