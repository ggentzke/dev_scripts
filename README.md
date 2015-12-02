# dev_scripts
Development Scripts

Collection of scripts that make developing easier, especially with git and github.

###.gitconfig###

Copy these into `~/.gitconfig` and enjoy the aliases via `git [alias]`.  Some clarifications:

Check a branch of pull request #123 a la `git copr 123`
`copr = !sh -c 'git checkout -b pr/$0 upstream/pr/$0'`

Print out the commit messages between your branch and a past release (in this case release_2015-10-31) a la `git release-notes 10-31`
`release-notes = !sh -c 'git log release_2015-$0..HEAD --format=%s --no-merges'`

Delete all branches except master.  Kind of a #YOLO move.
`master-blaster = !sh -c 'git branch | grep -v master | xargs git branch -D'`

I also suggest installing [gti](https://github.com/rwos/gti) which can be done via `npm install -g gti`.
