
# Git Extras

 Little git extra - now with even less little

## Installation

Clone / Tarball:

     $ make install

One-liner:

    $ curl https://github.com/robotarmy/git-extras/raw/master/bin/git-update-extras | sh

## Commands

 - git delete-submodule
 - git ignore
 - git release
 - git repl
 - git update-extras
 - git touch

## git-repl

 GIT read-eval-print-loop:

     $ git repl
     
     git> ls-files
     History.md
     Makefile
     Readme.md
     bin/git-changelog
     bin/git-count
     bin/git-delete-branch
     bin/git-delete-tag
     bin/git-ignore
     bin/git-release
     
     git> quit


## git-release

 Release commit with the given &lt;tag&gt;.
	
	$ git release 0.1.0
 
 Does the following:

   - Commits changes (to changelog etc) with message "Release &lt;tag&gt;"
   - Tags with the given &lt;tag&gt;
   - Pushes the branch / tags

## git-ignore

 To lazy to open up _.gitignore_? me too! simply pass some patterns:

    $ git ignore build "*.o" "*.log"
	... added 'build'
	... added '*.o'
	... added '*.log'

 Running `git-ignore` without a pattern will display the current patterns:
   $ git ignore
   build
   *.o
   *.log 

## git-delete-submodule &lt;name&gt;

  Deletes submodule _name_.

    $ git delete-submodule lib/foo

## git-update-extras

 Updates git extras. clones the repo to _/tmp/git-extras_, make installs, then cds back to the origin directory.

## git-touch [filename]

Call `touch` on the given file and add it to the current index. Used one-step creating new files.
