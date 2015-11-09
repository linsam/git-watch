git-watch
=========

A simplish script to "track" more than than just upstream.


Purpose
-------

Git allows one to set an upstream branch, which the branch, status, etc.
commands will use to let you know how far ahead and/or behind you are to that
upstream.

In small groups, people often want to know how their branch compares to more
than just the central "upstream" version (or, maybe there is not central
version).

This script adds the concept of "watched" branches. It will list ahead/behind
information for everything listed as a watch.


Usage
-----

Any refspec can be checked, though the common case is a remote tracking branch.

Add any refspecs you like to a branch's 'watch' configuration variable. They can
be space separated, entry separated, or both.

This script will attempt to list information about regularly configured
"upstream" branches using the current branch's 'remote' and 'merge'
variables, and will then list information about each listed watch refspec.


Example
-------

Bob, Alice, and Jack work on a project.

Bob has remotes named "alice" and "jack" that track the repositories of Alice
and Jack.

All three have a master branch that they work on.

Bob can run the following the watch the master branch of Alice and Jack
(assuming the default fetch rules weren't changed):

  git config --add branch.master.watch alice/master
  git config --add branch.master.watch jack/master

Now "git watch" will list something like

  Branch is master
  You are behind 'alice/master' by 3 commits
  You have diverged from 'jack/master'. Ahead 1, behind 2

This can also watch other local branches (e.g. comparing master to next), or
any refspec (watch a tag, or a specific commit sha1). 
