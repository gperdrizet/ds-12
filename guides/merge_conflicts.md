# Fixing merge conflicts

To fix a merge conflict, check-out the pull request locally and merge it manually, then push the changes back to the parent repository. You must have write permission on the repository you are trying to merge into. This can be done in a Codespace on the parent repository or on a clone of the parent repository on your own computer.

Make sure you have the latest changes from parent:main, then fetch the pull request to a new branch and check out:

```bash
git pull
git fetch origin pull/5/head:pull_request
```

Now you can merge the pull request locally:

```bash
git merge pull_request
```

And manually resolve any merge conflicts file-by-file. `git status` will tell you which files have conflicts. You will have to open Jupyter notebooks as text. Other file types (like .py and .md) don’t need any special treatment. Look for sections marked with `===` and `<<<` symbols:

```python
<<<<<<< HEAD
This is the content from the current local version of the file.
=======
This is the incomming content from the pull request on the same line(s) of the file.
>>>>>>> child-fork
```

Select the incoming or current version, or write something else entirely. Once you are done, remove the conflict markers, commit the changes. Then, delete the `pull_request` branch and push the changes back to the parent repository:

```bash
git add .
git commit -m “Merged pull request”
git branch -d pull_request
git push origin main
```bash

Done.
