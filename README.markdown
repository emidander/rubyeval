# rubyeval

## About

The simplest possible solution (maybe) to use ruby expressions instead of awk, sed and all the other tools whose syntax you will never remember.

## How?

To rename all files named file1.png, file2.png and so on to vacation1.png, vacation2.png, first do this:

    $ ls | rubyeval "'mv ' + f + ' ' + f.gsub(/file/, 'vacation')"
		mv file1.png vacation1.png
		mv file2.png vacation2.png

Verify the mv-command. If they look ok, add the -x parameter (execute):

    ls | rubyeval -x "'mv ' + f + ' ' + f.gsub(/file/, 'vacation')"
		mv file1.png vacation1.png
		mv file2.png vacation2.png

And that's it.

