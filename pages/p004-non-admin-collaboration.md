sharing work with assistants
================

![](../resources/near-future.jpg) <small> <br> <i>Near future</i> by
Anja Mexicola is licensed under
<a href="https://creativecommons.org/licenses/by-nc/2.0/legalcode">CC
BY-NC 2.0</a> <br> </small>

We start by assuming an **author** has created an RStudio “project” on
their local machine and has linked it to a GitHub repository (a “repo”).
The author is ready to share work with an **assistant**. Both author and
assistant should have completed the [Installing
software](p001-install-software.md) instructions.

In this approach, the assistant’s work is submitted to the project as a
pull request that requires review by the author (or other project
administrator) before acceptance.

## contents

-   [Author’s initial tasks](#authors-initial-tasks)
-   [Assistant’s initial tasks](#assistants-initial-tasks)
-   [Synchronizing the work](#synchronizing-the-work)
-   [Branch](#branch)
-   [Commit](#commit)  
-   [Pull from and push to the fork](#pull-from-and-push-to-the-fork)
-   [Pull request](#pull-request)

## author’s initial tasks

-   Make the GitHub repo public  
-   Provide the repo URL to the assistant

## assistant’s initial tasks

The assistant “forks” and “clones” the project as follows.

-   Navigate to the project repo using the URL provided by the project
    admin
-   Click the *Fork* button and select the destination (typically your
    GitHub account)  
-   Navigate to your GitHub account and select the project repo (the
    fork) saved there
-   *Code* pulldown menu and copy the URL, for example:

![](../resources/git-collab-001.png)

-   Keep the URL in your clipboard or save it locally in a temporary
    text file
-   Launch RStudio
-   *File &gt; New Project* and select *Version Control*

![](../resources/git-collab-002.png)

-   Select *Git*

![](../resources/git-collab-003.png)

-   In the dialog box, paste the *Repository URL* you saved earlier
-   The *Project directory name* is auto-filled
-   Use the *Browse* button to select the local directory for storing
    the project files
-   Click the *Create project* button

![](../resources/git-collab-004.png)

The assistant now has a local repo that matches the fork they created.

## synchronizing the work

As the figure illustrates, the assistant forks and clones the project.
The assistant can pull and push to their own remote repo on GitHub but
they must initiate a pull request to transmit their proposed changes to
the main project repo where it is reviewed before acceptance.

![](../resources/git-collab-010.png)

## branch

Because you will be submitting changes to the project owners for review,
they will be happier to receive your pull request from a non-main
branch.

Therefore, before beginning any work on your copy of the project, work
in a new branch, not the main branch.

<!-- If you make any commits in your local repository, I strongly recommend that you work in a new branch, not master. -->
<!-- I strongly recommend that you do not make commits to master of a repo you have forked. -->
<!-- This will make your life much easier if you want to pull upstream work into your copy. The OWNER of REPO will also be happier to receive your pull request from a non-master branch. -->

## commit

Let’s assume you have edited the project files on your local machine. In
RStudio, select the Git tab, for example,

![](../resources/git-collab-006.png)

Check all the boxes in the *Staged* column.

![](../resources/git-collab-007.png)

Click on *Commit*. In the dialog box, type a short description of the
changes. Click the *Commit* button.

![](../resources/git-collab-008.png)

Close the commit windows that appear.

Commit your work often.

## pull from and push to the fork

When the assistant is ready to synchronize their work, first do a final
commit if there are any unstaged changes.

Next, pull from the fork (the assistant’s primary repo) by clicking
*Pull* in

-   the Review Changes window, or
-   under the Git tab

![](../resources/git-collab-011.png)

A *Git Pull* window appears. The message will describe changes since the
last time you pulled from the fork.

Select *Push* to send your changes to your GitHub repo (not the main
project repo). A *Git Push* window appears with a message on the status
of the push. You can close the window.

To confirm that your changes have been correctly pushed, navigate to the
GitHub fork. You should find that the remote repository contains your
recent edits.

## pull request

------------------------------------------------------------------------

<a href="#top">▲ top of page</a>  
[◁ main page](../README.md)
