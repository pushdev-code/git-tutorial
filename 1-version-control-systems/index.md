# Introduction to version control systems

Let's see what we can do with VCS, and how it will benefit our developer skills.

## What are Version Control Systems?

A version control system (VCS) is a piece of software that records files and the changes in those files so you can switch in between specific versions later. The collection of versions are saved in a place called repository so they are tracked into a captured snapshot at certain point in time.

![Version control systems](https://www.vogella.com/tutorials/Git/img/xvcs_state10.png.pagespeed.ic._BJgeBXw1P.webp)
Source: [Vogella](https://www.vogella.com/tutorials/Git/article.html#introduction-into-version-control-systems)

Simple: Think about VCSs as a software that tracks all the changes you make to certain group of files so you can revert any change at any time. No more files named: `final-draft1-copy-this-is-final-now-correct-final-1`

## Version control concepts

Basic Setup

* __Repository (repo):__ The database storing the files.
* __Server:__ The computer storing the repo.
* __Client:__ The computer connecting to the repo.
* __Working Set/Working Copy:__ Your local directory of files, where you make changes.
* __Trunk/Main:__ The primary location for code in the repo. Think of code as a family tree — the trunk is the main line.

Basic Actions

* __Add:__ Put a file into the repo for the first time, i.e. begin tracking it with Version Control.
* __Revision:__ What version a file is on (v1, v2, v3, etc.).
* __Head:__ The latest revision in the repo.
* __Check out:__ Download a file from the repo.
* __Check in:__ Upload a file to the repository (if it has changed). The file gets a new revision number, and people can “check out” the latest one.
* __Checkin Message:__ A short message describing what was changed.
* __Changelog/History:__ A list of changes made to a file since it was created.
* __Update/Sync:__ Synchronize your files with the latest from the repository. This lets you grab the latest revisions of all files.
* __Revert:__ Throw away your local changes and reload the latest version from the repository.

Advanced Actions

* __Branch:__ Create a separate copy of a file/folder for private use (bug fixing, testing, etc). Branch is both a verb (“branch the code”) and a noun (“Which branch is it in?”).
* __Diff/Change/Delta:__ Finding the differences between two files. Useful for seeing what changed between revisions.
* __Merge (or patch):__ Apply the changes from one file to another, to bring it up-to-date. For example, you can merge features from one branch into another.
* __Conflict:__ When pending changes to a file contradict each other (both changes cannot be applied).
* __Resolve:__ Fixing the changes that contradict each other and checking in the correct version.
* __Locking:__ Taking control of a file so nobody else can edit it until you unlock it. Some version control systems use this to avoid conflicts.
* __Breaking the lock:__ Forcibly unlocking a file so you can edit it. It may be needed if someone locks a file and goes on vacation (or “calls in sick” the day Halo 3 comes out).
* __Check out for edit:__ Checking out an “editable” version of a file. Some VCSes have editable files by default, others require an explicit command.

And a typical scenario goes like this:

Alice __adds__ a file (`list.txt`) to the __repository__. She __checks it out__, makes a change (puts “milk” on the list), and checks it back in with a checkin message (“Added required item.”). The next morning, Bob __updates__ his local working set and sees the latest revision of `list.txt`, which contains “milk”. He can browse the __changelog__ or __diff__ to see that Alice put “milk” the day before.

Source: [Better explained](https://betterexplained.com/articles/a-visual-guide-to-version-control/)


development class 1