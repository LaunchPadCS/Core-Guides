## An introduction to Git and Github

Git is used *everywhere* in software development, because it allows teams and groups of people to collaborate. At its core, Git is a way of keeping track of code changes, and is known as a **version control system**. Being able to interact with Git is vital to software development.

### Diving into Git

A lot of people get terms "Git" and "Github" confused, because sometimes they are used interchangeably. **Git** is the version control system that stores the history of your code, and by default, runs "locally" on your computer. **Github** allows you to host your Git repository online, where others can access it. Think of it as storing  a photo on your computer, and storing a photo on Dropbox.

To start off with Git, you need to first create a Git repository. A repository is where your project will live, and is contained in a folder. To create a repository, create a new folder, and type `git init` in your terminal. You now have a Git repository, and a *working tree*! Try creating a file in your newly created repository. Now, type `git status`. You should see a bunch of output, with your new file under the "Untracked files" section. In Git, there are several states that a file can be in.

| State     | Description                              |
| --------- | ---------------------------------------- |
| Untracked | File is not being tracked by your repository. Often because the file is new, and hasn't been committed yet. |
| Tracked   | File has been committed and is not staged. |
| Staged    | File has been staged, and is ready to be added to a new commit. |
| Modified  | The file has been changed, but hasn't been staged. |

Adding a file to your git repository with `git add` is fairly straight forward. You can add individually changed files, several changed files, or even all changed files with `git add`. To stage all new files, modified files, and deleted files, you would  run `git add .`

Once you've added (staged) files, you need to commit them to your repository. To commit, you can run `git commit -m "<message>"`. The message is used to keep track of what changes you've made in the commit, so be sure to make them useful, eg. "Fixed render() crash". Once you've committed with your message, run `git log`, and you should see your commit in the history!

### Branching

Branching is a slightly more advanced feature of Git, and it is incredibly useful when working in a larger team, with multiple different features. Branching allows you to create a new, separate working tree from the main, or master branch. For example, if user A and user B wanted to create two features from the current codebase, they would create a branch off the master branch, called "feature1" and "feature2". When both users finish their branches, both users would *merge* their branches back into master. This allows the two users to complete work independently, without messing up the master branch with potentially unfinished features. For more information on branching, check [this git guide.](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)

### Using Github

As discussed earlier, Github is a place where you can host your git repositories. Now, Github is even used as a portfolio, where you can show off your projects and open source contributions. To get started on Github, [create an account](https://github.com/), and then create a repository. Once you've made the repository, you can "link" the local repository we made earlier with Github, by running the `git remote add origin https://github.com/...` command listed. The only difference in using Github is that you must now run `git push` after committing to upload your changes to Github.

### Conclusions

Now you know how to use git at a basic level. We recommend taking a look at the resources below to familiarize yourself further with git. Git is one of those things that you could spend hours and hours learning, but at the end of the day, you really only need to know a little bit to get started. Regardless of your comfort level with git, it's important that you use it from day one, so that you can incrementally learn new features of git as you need them.

### Recommended Reading

[git-scm book](https://git-scm.com/book/en/v2/)

[Learn Git by CodeCademy](https://www.codecademy.com/learn/learn-git)

[Git Resources by Atlassian](https://www.atlassian.com/git)

