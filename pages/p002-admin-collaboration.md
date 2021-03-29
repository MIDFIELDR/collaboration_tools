collaboration among co-authors
================

We start by assuming an **author** has created an RStudio “project” on
their local machine and has linked it to a GitHub repository (a “repo”).
The author is ready to invite a **co-author** to collaborate. Both
author and co-author should have completed the [Installing
software](p001-install-software.md) instructions.

In this approach, author and co-authors all have the ability and
authority to edit project files.

## contents

-   [Author’s initial tasks](#authors-initial-tasks)
-   [Co-author’s initial tasks](#co-authors-initial-tasks)
-   [Workflow](#workflow)
-   [Synchronizing work](#synchronizing-work)

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

## workflow

As the figure illustrates, each worker has their own repository on their
local machine and GitHub is used as the single common repository for
coordination. Thus the GitHub repo is the main or primary record of the
project.

![](../resources/git-collab-005.png)

## synchronizing work

Typically, different authors may be working on different files in the
project at the same time. To synchronize the work, all authors follow
the steps described here.

**Commit**

On your local machine, in RStudio, select the Git tab, for example,

![](../resources/git-collab-006.png)

Check all the boxes in the *Staged* column.

![](../resources/git-collab-007.png)

Click on *Commit*. In the dialog box, type a short description of the
changes. Click the *Commit* button.

![](../resources/git-collab-008.png)

------------------------------------------------------------------------

<a href="#top">▲ top of page</a>  
[◁ main page](../README.md)
