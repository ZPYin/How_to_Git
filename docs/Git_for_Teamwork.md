# Git for Teamwork

## Changing a commit message

If a commit message contains unclear, incorrect, or sensitive information, you can amend it locally and push a new commit with a message to GitHub. You can also change a commit message to add missing information.

### Rewriting the most recent commit message

You can change the most recent commit message using the `git commit --amend` command.

>In Git, the text of the commit message is part of the commit. Changing the commit message will change the commit ID -- i.e., the SHA1 checksum that names the commit. Effectively, you are creating a new commit the replaces the old one.

#### Commit has not been pushed online

If the commit only exists in your local repository and has not been pushed to GitHub, you can amend the commit message with the `git commit --amend` command.

1. On the command line, navigate to the repository that contains the commit you want to amend.
2. Type `git commit --amend` and press **Enter**
3. In your text editor, edit the commit message, and save the commit.
    - You can add a co-author by adding a trailer to the commit. For more information, see [Creating a commit with multiple authors](https://help.github.com/en/articles/creating-a-commit-with-multiple-authors)
    - You can create commits on behalf of your organization by adding a trailer to the commit. For more information, see [Creating a commit on behalf of an organization](https://help.github.com/en/articles/creating-a-commit-on-behalf-of-an-organization)

The new commit and message will appear on GitHub the next time you push.

> You can change the default text editor for Git by changing the `core.editor` setting. For more information, see [Basic Client Configuration](https://git-scm.com/book/en/Customizing-Git-Git-Configuration#_basic_client_configuration) in the Git manual.

### Amending older or multiple commit messages

If you have already pushed the commit to GitHub, you will have to force push a commit with an amended message

> We strongly discourage force pushing, since this changes the history of your repository. If you force push, people who have already cloned your repository will have to manually fix their local history. For more information, see [Recovering from upstream rebase](https://git-scm.com/docs/git-rebase#_recovering_from_upstream_rebase) in the Git manual.

### Amending the message of the most recently pushed commit

1. Follow the [steps above](#rewriting-the-most-recent-commit-message) to amend the commit message.
2. Use the `push --force` command to force push over the old commit.

    ```bash
    git push --force branch-name
    ```

### Amending the message of older or multiple commit messages

If you need to amend the message for multiple commits or an older commit, you can use interactive rebase, then force push to change the commit history.

1. On the command line, navigate to the repository that contains the commit you want to amend.
2. Use the `git rebase -i HEAD~n` command to display a list of the last `n` commits in your default text editor.

    ```bash
    git rebase -i HEAD~3   # display a list of the last 3 commits
    ```

3. Save and close the commit list file.
4. In each resulting commit file, type the new commit message, save the file, and close it.
5. Force-push the amended commits.

   ```bash
   git push --force
   ``` 

---
> All the documents come from [GitHub Help](https://help.github.com/en/github/committing-changes-to-your-project/changing-a-commit-message)
