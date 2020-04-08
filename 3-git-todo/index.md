# Create your own repository with your changes

We'll start practicing what we've learnt by creating a github repository and making our changes available through it.

1. Use or create your [github](https://github.com/) account.
2. [Download Git](https://git-scm.com/downloads) if it's not already installed in your system.
3. Open your computer's Terminal and type `git`.
If everything is ok you should not see any error message.
4. go to your documents directory and create a new folder for this training.

```
$ cd documents
$ mkdir push-dev
$ cd push-dev
```

5. By staying at the `push-dev` folder, Clone this repo:

```
$ git clone https://github.com/pushdev-code/git-tutorial.git
$ cd git-tutorial
```
6. Create a new branch with following this name convention:

```
$ git checkout -b feature/your-full-name
```

7. go to 4-students folder and create a markdown file using your name:

```
$ cd 4-students
$ touch your-full-name.md
```

Edit this file and include some comment about your opinion on Git.

*Note*: `touch` command won't work on Windows, use `echo.> your-full-name.md`.

8. Add this file to the repository:

```
$ git add 4-students/your-full-name.md
```

9. Commit your changes, including a good commit message:

```
$ git commit -m "Include a meaningful description of your changes"
```

10. Make sure to share your github username with us so you can be a collaborator and have permissions to push code and create Pull Requests, they will be necessary for the upcoming steps.

11. Push your changes to the remote branch:

```
$ git push -u origin feature/your-full-name
```

12. Go to [https://github.com/pushdev-code/git-tutorial](https://github.com/pushdev-code/git-tutorial) and create a new Pull request. The button for your branch should appear when the page has loaded. If the button doesn't appear, click on pull requests link.

* Make sure your Pull request base is the `master` branch.
* Please include `fabianmarinog` and `juancho11gm` as reviewers so we can approve your changes.
* Wait until the Pull request is merged into master.

13. To see your changes in the `master` brannch:

```
$ git checkout master
$ git pull
```

That's it. Your changes should be now part of the main `master` branch.
