## Git test

**Concepts**
* Explain Git in simple terms. What kind of problems does it help solve?
* Describe the difference between a local repository and a remote repository.
* What is the purpose of "staging" changes in Git?
* Explain the basic workflow of making changes, committing them, and optionally pushing them to a remote repository.
* What is a Git branch, and why are branches useful?

**Git Commands**
* **Initializing a repository:**  How would you create a new local Git repository in a directory?
* **Staging and Committing:** 
    * How do you stage all changes in your working directory?
    * How do you commit staged changes with a commit message?
* **Checking Status:**  What command shows the status of your current branch, including staged and unstaged changes?
* **Branching**
    * How do you list all existing branches in your repository?
    * How do you create a new branch and switch to it?
* **Basic History:**  How would you view a log of recent commits in your repository? 
* **Beyond the Basics:**  Explain the use of these commands:
    * `git rebase` (and how it differs from merge)
    * `git cherry-pick` 
    * `git bisect`
    * `git stash` 
* **Workflows:** Describe a real-world scenario for when you would use each of the commands above.
* **Fixing Mistakes:**  You've accidentally committed sensitive data. How could you use Git commands to remove it from the repository's history?
* **Untangling Changes:** You need to revert a series of recent commits but preserve the changes locally for later. What Git commands would help?
* **Collaboration:** Briefly describe how you would use `git pull --rebase` to integrate remote changes while keeping a clean commit history.

---
### Questions with Answers
Let's break down some essential Git concepts with questions and answers focused on cloning, initializing, and understanding their purpose.

**Cloning**
* **Q: What does it mean to "clone" a Git repository?**
   * **A:** Cloning means creating a local copy of a remote Git repository on your own computer.  This includes the project's entire version history and files.

* **Q: Why would I want to clone a repository?**
   * **A:**  Reasons to clone include:
        * **Collaborating on a project:** Get the code to make changes and contribute back.
        * **Working offline:** Develop features independently before pushing them to the remote repository.
        * **Exploring an existing codebase:**  Analyze the structure and history of a project. 

* **Q: How do I actually perform a clone?**
   * **A:** Typically, you use the `git clone` command followed by the URL of the remote repository.  Example: 
     ```bash 
     git clone https://github.com/mfel-it/knowledgebase.git
     ```

**Initializing**

* **Q: What is the purpose of initializing a Git repository?**
   * **A:** Initializing creates a hidden `.git` folder within a project directory. This folder is where Git stores all the information to track changes, history, and branches for your project.

* **Q: When should I initialize a repository?**
   * **A:**  Initialize when:
        * **Starting a new project:**  Set up Git version control from the beginning.
        * **Existing project without Git:**  You want to start tracking changes in a project that wasn't previously under Git control.

* **Q: How do I initialize a repository?**
   * **A:** Navigate to your project's root directory and use the command:
      ```bash
      git init 
      ```
**Understanding Branches**

* **Q: What is a Git branch?**
  * **A:** A branch is a separate line of development in your Git repository. It allows you to work on new features or bug fixes without affecting the main codebase.

* **Q: When should I use branches?**
  * **A:** Use branches to:
      * Isolate feature development: Work on a new feature without interfering with the main code.
      * Fix bugs: Create a separate branch to isolate a bug fix without affecting ongoing work.
      * Experiment with changes: Try out new ideas without affecting the stable codebase.

* **Q: How do I create and switch between branches?**
  * **A:**  Use the following commands:
      * `git branch <branch_name>` to create a new branch.
      * `git checkout <branch_name>` to switch to an existing branch.

**Adding and Committing Changes**

* **Q: What does "staging" mean in Git?**
  * **A:** Staging refers to selecting specific changes you made to files and marking them ready to be included in your next commit.

* **Q: How do I stage and commit changes?**
  * **A:** Use these commands:
      * `git add <file_name>` to stage a specific file.
      * `git add .` to stage all modified files in the current directory.
      * `git commit -m "<commit message>"` to create a commit with a descriptive message summarizing your changes.

**Pushing and Pulling**

* **Q: What does "pushing" to a remote repository mean?**
  * **A:** Pushing sends your local commits to a remote Git repository, typically hosted on a platform like GitHub. This shares your changes with collaborators or makes them publicly available.

* **Q: When would you use "pulling" from a remote repository?**
  * **A:** Pulling retrieves the latest changes from the remote repository and merges them into your local branch. This is important to keep your local copy up-to-date with changes made by others. 

* **Q: How do I push and pull changes?**
  * **A:** Use these commands:
      * `git push origin <branch_name>` to push your local commits from a specific branch to the corresponding branch on the remote repository named "origin" (often the default).
      * `git pull origin <branch_name>` to pull the latest changes from the remote branch "branch_name" and merge them into your local branch.

**Understanding 'git fetch'**

* **Q: What does `git fetch` actually do?**
   * **A:** `git fetch` downloads the latest changes (commits, branches, and refs) from a remote repository *without* merging them into your local working copy. It updates your local knowledge of the remote repository's state.

* **Q: Why is `git fetch` important, and how does it differ from `git pull`?**
   * **A:**  It gives you a chance to review and compare the remote changes before deciding how to integrate them.  `git pull` is essentially a `git fetch` followed by an immediate `git merge`.

* **Q: Can you give a common use case for `git fetch`?** 
   * **A:** Before starting to work on a feature, you might use `git fetch origin main` to fetch the latest updates from the main branch of the remote named "origin", letting you see if there are any conflicts you need to resolve before integrating your own changes.

**Unveiling 'git sync' (and why it's less common)**

* **Q: What is `git sync`?**
   * **A:**  `git sync` is a less frequently used command that aims to combine the actions of  `git fetch` with other operations to update your local repository.  However, its exact behavior depends on how your specific Git hosting platform might have implemented it.

* **Q: Why is `git sync` less commonly discussed?**
   * **A:**
       * **Not a Core Git Command:** It's not a standard, built-in Git command. 
       * **Platform-Specific:**  Some Git hosting services (e.g., GitHub in the past)  might have provided `git sync` as a custom shortcut for specific workflows.

* **Q: Do I generally need to use `git sync`?**
   * **A:**  Likely not. The core commands  `git fetch`, `git pull`, and `git push` give you more granular control and are universal to Git. 

**Additional questions**

**Q: What's the difference between `git add` and `git commit`?**

* `git add`: Stages selected changes into a snapshot that's ready to be committed. This allows you to group related changes together.

* `git commit`:  Permanently records the staged snapshot into your project history.  Each commit should have a clear commit message summarizing the changes.

**Q:  How do you create a new branch and switch to it?**

   * `git branch <new-branch-name>`: Creates the new branch.
   * `git checkout <new-branch-name>`: Switches to the newly created branch.
   * **Shortcut:** `git checkout -b <new-branch-name>` does both in one step.

**Q:  I made changes on the wrong branch! How do I move them?**

* **Two common ways:**
    * **Stashing:** If it's temporary:
        * `git stash`: Temporarily saves your changes.
        * `git checkout <correct-branch>`  
        * `git stash pop`: Reapplies the stashed changes to the correct branch.  
    * **Committing and Cherry-picking:** For more permanent moves:
        * `git commit -m "My changes"` (on the wrong branch)
        * `git checkout <correct-branch>`
        * `git cherry-pick <commit-id>` (Find the commit-id using `git log`)

**Q: How do I view the history of changes in my project?**

* `git log`: Displays a list of commits with their IDs, timestamp, author, and commit messages. Use options for customization:
  * `git log --oneline`: Condensed one-line view.
  * `git log --graph`: Shows branching structure visually.

**Q: How do I undo a recent commit that hasn't been pushed?**

* `git reset`: Use with care! There are different modes:
  * `git reset --soft HEAD^`: Uncommits but keeps the changes staged.
  * `git reset --mixed HEAD^`: Uncommits and unstages changes (the default).
  * `git reset --hard HEAD^`: Discards the commit and its changes. 

---
**Scenario-Based**
* You made accidental changes to a file. How could you use Git to revert those changes and go back to the last commit?
* You've been working on a new feature in a separate branch.  Outline the steps on how to merge this completed feature into your main branch.

**Refining History**
* **Interactive Rebase:** You need to clean up a messy local branch before sharing it.  Describe how you'd use `git rebase -i` to squash commits, reword commit messages, and reorder changes.
* **Removing History:**  Explain the scenario where `git filter-branch` is the appropriate tool to remove a large file accidentally committed to your repository, and outline the potential risks involved.
* **Submodules vs. Subtrees:**  Both can manage external code within a repo.  Detail the key differences and use cases where you'd favor one over the other.

**Troubleshooting & Forensics** 
* **Lost Work:**  A developer says they've lost commits.  Describe at least two ways to potentially recover their work using Git's internal tools (e.g., reflog).
* **The Case of the Vanishing Change:**  Debugging showed a feature to be working, but now it's broken.  Outline how you'd use `git bisect` to narrow down which commit introduced the regression.
* **Blame with Context:**  `git blame` tells you *who* changed a line, but not *why*.  How would you dig deeper to find the commit that explains a change's reasoning?

**Workflows & Collaboration**
* **Customizing Git:** You find yourself frequently re-typing long Git commands with specific flags.  Explain how Git aliases or scripts could improve your workflow.  
* **Review Workflow:** Your team wants to adopt code reviews via Pull/Merge Requests.  Describe the pros, cons, and branch management implications of different review workflows (e.g., linear vs. forking).
* **Merge Strategies:**  Explain a situation where a recursive merge strategy might be more appropriate than the default fast-forward strategy, and outline potential trade-offs.

## Git Internals

**Beyond the Basics**
* **Hooks:** Describe a real-world use case for Git hooks (pre-commit, post-receive, etc.) to automate tasks or enforce quality checks.
* **Internals (Optional):**  High-level, explain how Git stores objects (blobs, trees, commits) and how this differs from centralized version control systems.

**Conceptual Knowledge**
* **Object Types:** Explain the three core object types Git uses (blob, tree, commit) and how they relate to each other.
* **Not Just Diffs:** Many VCS systems store diffs. How does Git's content-addressable object storage fundamentally differ in its approach? 
* **Immutability:** In what way does the immutability of Git objects contribute to its reliability and performance?
* **.git Directory:** Briefly describe the contents and key files within a repository's hidden `.git` directory.

**References & the Reflog**
* **HEAD:** Explain the role of `HEAD` in Git.  How does it differentiate between a normal branch reference and a detached HEAD state?
* **Branch as Pointer:**  Explain that Git branches are essentially "lightweight pointers" to specific commits.
* **Dangling Objects:** Under what circumstances might Git create dangling objects? How would you potentially address this?
* **Reflog:**  Describe a scenario where the reflog would be instrumental in recovering from a Git mishap.

**Indexing & Compression**
* **The Index (Staging Area):** Explain the purpose of the Git index and how it works in the process of creating a commit.
* **Packfiles:** How does Git use packfiles to optimize repository storage, and what triggers their creation?
* **Delta Compression:**  At a high level, describe the idea of delta compression and how Git uses it to save space.

**Practical Implications**
* **"Cheap" Branches:** Git encourages lots of branches.  Explain how its internal design makes branching operations fast and efficient. 
* **Finding Large Files:** Even if deleted, large files bloat a repo's history. How might you use Git's object model to identify these culprits? 

