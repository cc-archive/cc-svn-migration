# CC Svn to Git migration

This repository contains some notes and a configuration file used to
migrate CC's Subversion repository to Git repositories, as part of a
migration to GitHub.

The tool used is the KDE project's <code>svn2git</code>. Beware, there
are other tools floating out there with the same name (!). Here are
some links to learn more about it:

* [A good overview of the tool and process](http://blog.smartbear.com/software-quality/migrating-from-subversion-to-git-lessons-learned/)
* [KDE docs for svn2git](http://techbase.kde.org/Projects/MoveToGit/UsingSvn2Git)
* [KDE rules for reference/examples](https://www.gitorious.org/svn2git/kde-ruleset/source/7125db355d730fc086ca0e03618017f879d54995:kde-rules-main#L2482-2807)
* [This post](http://www.patrickbougie.com/2013/03/18/convert-svn-to-git-repository) has notes for using a different svn2git tool, but some good info nonetheless.

To run the conversion, use the cc.rules file in this repository
against the CC svn repo. Note that you run it directly on the local
svn DB files, not via http. The logs folder contains logs for the
conversion we ran, just in case those are useful at any point in the
future.

The svn-props folder contains some info on svn properties used,
obtained by running <code>svn prop{list,get} -R</code> commands.

Once the git repositories are created locally, remote GitHub
repositories are created and uploaded to--see the create-gh-repos and
logs/upload-log.* files For details/logs. Note that we renamed some of
the repos when uploading to GitHub, because of naming conflicts or for
clarity.