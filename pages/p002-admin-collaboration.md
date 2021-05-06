using version control to share work
================

![](../resources/p002-header.jpg) <small> <br> <i>Network</i> by
gritphilm is licensed under
<a href="https://creativecommons.org/licenses/by-nc-nd/2.0/legalcode">CC
BY-NC-ND 2.0</a> <br> </small>

We start by assuming an **author** has created an RStudio “project” on
their local machine and has linked it to a GitHub repository (a “repo”).
The author is ready to invite a **co-author** to collaborate. Both
author and co-author should have completed the [Installing
software](p001-install-software.md) instructions.

In this approach, author and co-authors all have permission to make
changes without prior approval by another author.

If you want to learn more about using git and GitHub, see “Happy Git and
GitHub for the useR” \[[1](#ref-Bryan+Hester:2021)\] from which I
adapted most of this tutorial.

## contents

-   [Author’s initial tasks](#authors-initial-tasks)
-   [Co-author’s initial tasks](#co-authors-initial-tasks)
-   [Synchronizing the work](#synchronizing-the-work)
-   [Commit](#commit)
-   [Pull with rebase](#pull-with-rebase)
-   [Push](#push)

## author’s initial tasks

-   Obtain the co-author’s GitHub name or email address associated with
    their GitHub account
-   Navigate to the project repo on GitHub (the repo can be public or
    private)
-   Click on the *Settings* icon
-   Click on the *Manage access* tab
-   Click on the *Invite teams or people* button
-   Type the co-author’s GitHub name or email in the dialog box.

## co-author’s initial tasks

The co-author receives and accepts the invitation to collaborate.

The co-author “clones” the project as follows.

-   Navigate to the project repo.
-   *Code* pulldown menu and copy the project URL, for example:

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

The co-author now has a local repo that matches the main repo on GitHub.

## synchronizing the work

As the figure illustrates, each worker has their own repository on their
local machine and GitHub is used as the single common repository for
coordination. Thus the GitHub repo is the main or primary record of the
project.

![](../resources/git-collab-005.png)

## commit

Typically, different authors may be working on the project at the same
time. To synchronize the work, all authors follow the steps described
here.

On your local machine, in RStudio, select the Git tab, for example,

![](../resources/git-collab-006.png)

Check all the boxes in the *Staged* column.

![](../resources/git-collab-007.png)

Click on *Commit*. In the dialog box, type a short description of the
changes. Click the *Commit* button.

![](../resources/git-collab-008.png)

Close the commit windows that appear.

Commit your work often.

## pull with rebase

When you are ready to synchronize your work, first do a final commit if
you have any unstaged changes.

Next, under the Git tab, use the *Pull* pulldown menu to select *Pull
with Rebase*.

![](../resources/git-collab-009.png)

A *Git Pull* window appears. The message will describe changes since the
last time you pulled from the GitHub repo. Using pull with rebase, your
commits are applied on top of incoming changes.

## push

Select *Push* to send your changes to GitHub. A *Git Push* window
appears with a message on the status of the push. You can close the
window.

To confirm that your changes have been correctly pushed, navigate to the
GitHub repo. You should find that the remote repository contains your
recent edits.

## references

<div id="refs" class="references csl-bib-body">

<div id="ref-Bryan+Hester:2021" class="csl-entry">

1\. Bryan J, Hester J (2021) <span class="nocase">Happy Git and GitHub
for the useR</span>. <https://happygitwithr.com/>

</div>

</div>

------------------------------------------------------------------------

<a href="#top">▲ top of page</a>  
[◁ main page](../README.md)
