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

**Q1: What's the difference between `git add` and `git commit`?**
<details><summary>Answer</summary>

* `git add`: Stages selected changes into a snapshot that's ready to be committed. This allows you to group related changes together.

* `git commit`:  Permanently records the staged snapshot into your project history.  Each commit should have a clear commit message summarizing the changes.
</details>

**Q2:  How do you create a new branch and switch to it?**
<details><summary>Answer</summary>

   * `git branch <new-branch-name>`: Creates the new branch.
   * `git checkout <new-branch-name>`: Switches to the newly created branch.
   * **Shortcut:** `git checkout -b <new-branch-name>` does both in one step.
</details>

**Q3:  I made changes on the wrong branch! How do I move them?**
<details><summary>Answer</summary>

**Two common ways:**
    * **Stashing:** If it's temporary:
        * `git stash`: Temporarily saves your changes.
        * `git checkout <correct-branch>`  
        * `git stash pop`: Reapplies the stashed changes to the correct branch.  
    * **Committing and Cherry-picking:** For more permanent moves:
        * `git commit -m "My changes"` (on the wrong branch)
        * `git checkout <correct-branch>`
        * `git cherry-pick <commit-id>` (Find the commit-id using `git log`)
</details>

**Q4: How do I view the history of changes in my project?**
<details><summary>Answer</summary>

`git log`: Displays a list of commits with their IDs, timestamp, author, and commit messages. Use options for customization:
    * `git log --oneline`: Condensed one-line view.
    * `git log --graph`: Shows branching structure visually.
</details>

**Q5: How do I undo a recent commit that hasn't been pushed?**
<details><summary>Answer</summary>

`git reset`: Use with care! There are different modes:
    * `git reset --soft HEAD^`: Uncommits but keeps the changes staged.
    * `git reset --mixed HEAD^`: Uncommits and unstages changes (the default).
    * `git reset --hard HEAD^`: Discards the commit and its changes. 
</details>

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

