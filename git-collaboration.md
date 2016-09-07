# <img src="https://cloud.githubusercontent.com/assets/7833470/10899314/63829980-8188-11e5-8cdd-4ded5bcb6e36.png" height="60"> GitHub Collaboration Workflow


GitHub is a powerful tool for version control and collaborating on code.

## Branches

In Git, branches are a part of your everyday development process. When you want to add a new feature or fix a bug—no matter how big or how small—you spawn a new branch to encapsulate your changes. This makes sure that unstable code is never committed to the main code base, and it gives you the chance to clean up your feature’s history before merging it into the main branch.

Branches are incredibly lightweight "movable pointers" that help us as developers make experimental changes! A branch in git is just a label or pointer to a particular commit in a repository, along with all of it's history (parent commits).

What makes a branch special in git, is that we're always on a specific branch, and when we commit, the current branch HEAD moves forward to the new commit. Another way to say that is the HEAD always stays at the tip of the branch.

Terminology: HEAD is simply a reference to the current or most recent commit!



![image](https://cloud.githubusercontent.com/assets/6520345/15020568/663aa804-11d7-11e6-83f6-774e43bc2ea6.png)


Q. Why is branching an important part of git?
---

> A. Branches are useful for many reasons, but some of the most common ones:

> 1. To allow experimentation. By switching to a new branch, we can experiment,
and if the experiment fails, we can delete it and easily switch back to master
(or another branch of our choice). If it succeeds, we can merge those changes
into master.
2. To allow work to proceed on multiple features (or by multiple people) without
interfering. When a feature is complete, it can be merged back into master.
3. To allow easy bug fixes on a stable version while features are being developed.

## `git fetch`, `git merge`, and `git pull`

Fetching, merging, and pulling are related commands that you will frequently use to update your local repository to include your collaborator's work.

[`git fetch`](https://git-scm.com/docs/git-fetch) gets all of the updates from the remote repositories without changing the location of the local HEAD.

[`git merge`](https://git-scm.com/docs/git-merge) joins two different places in your development tree. This is frequently used to bring together your changes with the changes you just fetched. If you were on branch `add-auth` and you had just `git fetch`'d updates from the remote, you could then `git merge origin/add-auth`. This would join your changes and the changes that had been made to this branch on origin. You also commonly use merge to pull changes from one branch into another so that your current branch doesn't become out of date while you work.

[`git pull`](https://git-scm.com/docs/git-pull) is the combination of fetching and merging to the newly fetched version of the current branch.

## Resource: Git branching tutorial

Do Levels 1-3 of this [git branching tutorial](http://pcottle.github.io/learnGitBranching/). Stop at 4: "Rebase Introduction".
Take your time:
* Read all the dialogs. They are part of the tutorial.
* Think about what you want to achieve.
* Think about the results you expect before you press enter.
* Whenever you see/type `git commit`, you can assume some changes have been made and staged.

## Collaboration Workflow

There are two main scenarios for collaborating on coding projects:

1. You **fork** another developer's project and make pull requests from *your remote fork* to the *project's remote*.
2. Another developer makes you a **collaborator** on a project they own, giving you the ability to make pull requests directly from the project's *remote feature branches* to the project's *remote master*. (Note that as a collaborator on a project, you also have the ability to push directly to the master branch, which you should NEVER do.)

![github-collab-diagram](https://cloud.githubusercontent.com/assets/7833470/12072895/69abd404-b0b1-11e5-8d8c-4ff54c13b0a0.png)

## Collaborator Scenario

Imagine you, Jessica, and Ali want to build an app together. Jessica starts a project, pushes the initial code to GitHub, and adds the other two group members as <a href="https://help.github.com/articles/adding-collaborators-to-a-personal-repository" >collaborators</a>. The group delegates tasks and sets to work.

Your first task is to set up models for two resources. At the same time, Jessica is doing API integration and Ali is writing tests.

1. You clone the project Jessica pushed up to GitHub after she makes you a collaborator. This creates a local repository on your computer with a `remote` called `origin`, which is the original repo Jessica created.

2. Before you start creating models, make a new branch called `database-setup`. (Feature branches help organize work on a project and ensure that only production-ready code lives on the `master` branch.)

  ```zsh
     git checkout -b database-setup
  ```

  *Now, you complete your task, making frequent commits as you go. The following steps outline how to get your new code up to the main group project, once you're ready.*

3. Make sure you've committed your most recent changes on your `database-setup` branch. Switch back to your local `master` branch, then pull from `origin/master` to bring your local `master` branch up to date.

  ```zsh
     git checkout master
     git pull origin master
  ```

4. Now switch back to your local feature branch and merge your local `master` branch into it. This will give you a chance to resolve all conflicts with the most up-to-date master version before making a pull request. Watch git's output in the Terminal to see if any files have merge conflicts.

  ```zsh
     git checkout database-setup
     git merge master
  ```

  **VERY IMPORTANT:** IF you have a merge conflict, you should work through the instructions for [resolving merge conflicts locally](#resolving-merge-conflicts-locally) with a teammate.

5. Once you've resolved any conflicts, add and commit your changes locally. Push your feature branch to the remote `origin` repo.

  ```
     git add .
     git commit -m "fix conflicts; merge master into database-setup"
     git push origin database-setup
  ```

6. In your browser, head to the original remote repo's GitHub page (on Jessica's account). GitHub will detect that you just pushed a new branch and give you a prompt to make a pull request for that branch. Go for it!

  ![pull-request](https://cloud.githubusercontent.com/assets/7833470/12072813/76841710-b0aa-11e5-9644-4f840081c986.png)

  Someone else on the team should review your code and suggest any changes needed before merging it in.

7. If there are no other pull requests, one of your team members can merge your pull request cleanly with the most up-to-date `master`. However, if your team merges other pull requests before yours, those pull requests might create merge conflicts with yours.

  In that case, GitHub will show that merge conflicts exist and must be resolved locally. You'll want to repeat steps 3-5 to resolve the conflicts locally. Remember, it's up to each branch's owner to fix merge conflicts.

8. Once the `database-setup` feature branch has been moved into the `master` branch, you can delete the feature branch on GitHub. (If you really need to, you can restore the deleted branch through GitHub.)

9. Go back to your local `master` branch and pull the changes from the remote repo.

   ```
   git pull origin master
   ```

10. Congratulations! You're ready to start a new feature.

## Resolving Merge Conflicts Locally
1. First, and most importantly: Don't panic! Communication between team members will help you avoid them, but merge conflicts will inevitably happen. They're not the end of the world! Follow the rest of these steps to resolve conflicts.

2. When merging your local `master` branch into a local feature branch, the Terminal will let you know if there are conflicts, and if so, which files have conflicts.

  ![conflict-terminal](https://cloud.githubusercontent.com/assets/7833470/12072814/7a636df4-b0aa-11e5-98b0-0e31b37dc41d.png)

3. Open your project in your text editor, and open the file(s) with conflicts. You can see the conflict here on lines 27-33:

  ![conflict-sublime](https://cloud.githubusercontent.com/assets/7833470/12072816/813bd576-b0aa-11e5-9b22-b6b41302f9fa.png)

4. You AND one of your group members should decide together which version of the code to keep and which to delete. Remember to always delete the "merge junk" (`<<<<<<< HEAD`, `=======`, and `>>>>>>> master` lines) to prevent syntax errors.

  ![delete-code](https://cloud.githubusercontent.com/assets/7833470/12072817/842c5cce-b0aa-11e5-9c9a-9eecb678a7ad.png)

5. After deleting the decided-upon code and the merge junk, your file should now have the clean version of the code, ready to be checked into git.

  ![final-code](https://cloud.githubusercontent.com/assets/7833470/12072818/8760301e-b0aa-11e5-8248-9201c1d70153.png)

6. Add and commit your changes that resolved the conflict(s):

  ![resolve-conflict](https://cloud.githubusercontent.com/assets/7833470/12072819/898221a4-b0aa-11e5-84ec-f6a1bedaa6de.png)

  Your feature branch is now ready to be pushed up to GitHub, without conflicts!

## Tips for Working in Teams
1. Communicate,communicate, communicate! Before you start coding, it's important for your team to discuss roles, expectations, and timetables. Don't assume that everyone is on the same page or that problems will magically resolve themselves - take the time to plan first, and you'll be glad you did later.

2. As part of your planning process, choose who will set up the GitHub repository. This person will add everyone else in the team as collaborators.

3. Set guidelines for merging pull requests. How many people should review the pull requests before they're merged? Who will be in charge of merging pull requests? What branch should they be merged into?

4. Consider making a "develop" or "staging" branch to merge into instead of merging into the master branch. Once your app is complete, then you can merge your development branch into the master branch.

5. Make very descriptive commit messages! The team members who are reading them should be able to tell at a glance what you were working on.

6. Clearly delineate who's working on what. Things will go much more smoothly if team members work on features that don't overlap. This is especially important if you're not all working in the same spot. It's easy to check in on one another when you're in the same room, but once people spread out it's not uncommon for wires to get crossed!

7. Don't have multiple team members working on the same feature branch at one time. If you're pair programming with someone, only use one computer to avoid having differing code on the same branch.

8. When merge conflicts arise, it's not up to the GitHub master to resolve them. It's up to the individual contributor! Follow the steps for [resolving merge conflicts locally](#resolving-merge-conflicts-locally), make sure to delete any merge junk from your code, and then push your cleaned-up branch to GitHub.  


## Resources

* <a href="https://help.github.com/articles/adding-collaborators-to-a-personal-repository" >Adding collaborators to a personal repository</a>
* <a href="http://nvie.com/posts/a-successful-git-branching-model" >A successful Git branching model</a>
* <a href="https://help.github.com/articles/using-pull-requests" >Using pull requests</a>

## Git Tutorials

* <a href="https://www.codeschool.com/courses/try-git" >Try Git - Code School</a>
* <a href="https://github.com/Gazler/githug" >githug</a>
