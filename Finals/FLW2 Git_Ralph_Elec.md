![image](https://github.com/user-attachments/assets/fd267f2b-3077-458c-a66c-5d1238143148)


# SYSADM1 -- Git Basics

Answer the following research questions about Git, GitLab desktop and
GitHub.

1.  What is Git, and why is it important in software development?

-   *Git is a data protocol for managing and tracking changes in source
    code during software development, with all versions having unique
    hash codes. It enables teams to work together effectively, manage
    different versions of a project, and maintain the integrity of the
    code base. Modern software projects leverage the speed, branching
    capabilities, and robust history tracking of Git.*

2.  How does Git track changes in a project?

-   *Git captures the state of your project at a point in time across
    history through snapshots known as commits. These snapshots are the
    state of all files, and Git stores only what changed from the
    previous version, referencing it to earlier versions. With this
    procedure, project history is recorded in detail and can be easily
    accessed by any of its versions.*

3.  What is the difference between a local repository and a remote
    repository in Git?

-   *A local repository lives on a developer computer that archives the
    history of your project with its files for offline viewing. On the
    other hand, a remote repository exists on a server (for example
    GitHub or GitLab) and is used as a shared common ground for
    collaboration. When two teams are working on a project, developers
    sync changes between the two.*

4.  What are the basic Git commands?

**Repository Management**

-   git init: Initializes a new Git repository.

-   git clone \[url\]: Creates a local copy of a remote repository.

-   git remote add \[name\] \[url\]: Connects a local repository to a
    remote repository.

**File Tracking**

-   git add \[file/folder\]: Stages changes to be committed.

-   git rm \[file\]: Removes a file from the working directory and
    stages the deletion.

-   git mv \[source\] \[destination\]: Moves or renames a file.

**Saving Changes**

-   git commit -m \"\[message\]\": Saves staged changes with a message
    describing the changes.

-   git commit \--amend: Edits the last commit.

**Branching**

-   git branch: Lists all branches.

-   git branch \[branch-name\]: Creates a new branch.

-   git switch \[branch-name\]: Switches to a specified branch.

-   git checkout \[branch/file\]: Switches branches or restores a file
    from a branch.

**Synchronization**

-   git fetch: Retrieves changes from the remote repository but doesn't
    apply them.

-   git pull: Fetches and integrates changes from the remote repository.

-   git push: Uploads local changes to a remote repository.

-   Inspection and Comparison

-   git status: Displays the state of the working directory and staging
    area.

-   git diff: Shows the differences between the working directory and
    staged changes.

-   git log: Displays the commit history.

**Undoing Changes**

-   git reset \[file\]: Unstages a file while retaining its changes.

-   git revert \[commit\]: Creates a new commit to undo changes from a
    previous commit.

-   git stash: Temporarily saves changes for later use.

-   Tagging

-   git tag \[tag-name\]: Creates a tag for a specific commit.

**Help**

-   git help \[command\]: Displays help information for a specific
    command.

5.  How do you check the status of a Git repository?

-   *The "git status" command will give an overview of the current
    status of the repository. It will show the changes, untracked files
    and any modifications that has not been committed yet. This will
    allow the users to monitor the work that has been done and check
    whether they are in the correct file or not.*

6.  What is the purpose of branches in Git, and how do you create and
    switch between them?

-   *Branches in Git are essential since it helps the developers to have
    different lines of work with the main project. To create a branch
    enter "git branch \[branch-name\]", and to switch, enter "git
    checkout \[branch-name\]" or "git switch \[branch-name\]". This
    makes it possible to work concurrently, for instance, developers
    test some features before integrating them to the source code​*

7.  What are GitLab Desktop and GitHub, and how are they different from
    Git?

-   *GitLab Desktop and Github are applications used to monitor Git
    repositories and other features including issues and project
    pipelines. Git is a version control systems, while GitLab and GitHub
    extend the collaboration systems for teams for online managing
    projects but they are not same for features and integration.*

8.  How do you connect a local Git repository to a GitLab or GitHub
    repository?

-   *To connect a local repository to a remote one, you must use
    keywords: "git remote add origin \[repository URL\]" Then, safer
    push changes with "git push -- u origin \[branch name\]". Where the
    implementation's connections need to be secure, authentication
    protocols like SSH or HTTPS have to be implemented.*

9.  What are the steps to collaborate with others using GitLab or
    GitHub?

-   *In order to collaborate you have to create a clone of the
    repository, launch branches for particular operations, commit, and
    push to the remote repository. You will also need pull or merge
    requests to enable the developer to examine the contributions made
    by other contributors, and then decide whether or not to merge them
    into the project.*

10. How do you resolve merge conflicts in Git?

-   *Merge conflict will occur when two branches are being developed
    independently and there are changes in both. To fix them, Git marks
    files that have been changed in both branches, then the developers
    merge the changes manually. Sometimes the conflicts reached when
    using merge command, then use "git add" to stage the results and
    "git commit" for the final merge.*

11. What is a pull request, and why is it used in GitHub?

-   *A pull request is a technique used in repositories as a tool for
    suggesting changes and is particularly used when making changes that
    can be discussed. They can use it to make certain that latest code
    addition conforms to agreed upon project standards before
    integrating it into the master branch, meaning improved teamwork and
    code quality.*

12. What are some best practices for writing commit messages?

-   *Effective commit messages are brief and informative and contain
    what was done, and why it was done. They may come in a format, with
    a brief heading then a description if necessary. Good commit
    messages enable one to follow up on a project's history in terms of
    who did what and where to find problems.*

**REFERENCES:\
<https://phoenixnap.com/kb/what-is-git>\
<https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F>**
