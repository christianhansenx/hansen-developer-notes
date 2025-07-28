# git (my notes)

## LF
    git config --global core.autocrlf false
    https://stackoverflow.com/questions/71995658/how-to-stop-github-desktop-from-changing-my-line-endings
    REMEMBER TO ALSO CONFIGURE WINDOWS TO ENSURE THAT GITHUB DESKTOP TO USE IT

    To list configurations:
    git config --global --list --show-origin
    https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/The-global-Git-config-files-key-settings-and-usages#:~:text=To%20see%20all%20of%20properties,gitconfig%20file's%20location.

    https://stackoverflow.com/questions/2517190/how-do-i-force-git-to-use-lf-instead-of-crlf-under-window

    https://docs.github.com/en/get-started/getting-started-with-git/configuring-git-to-handle-line-endings

## Delete whole commit history
https://blog.avneesh.tech/how-to-delete-all-commit-history-in-github

Create a new branch
git checkout --orphan new_main

Add all the files
git add .

Commit the changes
git commit -m "commit message"

Delete the main/master branch
git branch -D main

Rename the current branch to main
git branch -m main

Finally, force update your repository
git push -f origin main

## Several github accounts (Windows)
Open Credential Manager:
Press Windows Key + S (or click the Start button and start typing).
Type "Credential Manager" and open the application.
Go to Windows Credentials:
In the Credential Manager window, make sure you click on the "Windows Credentials" tab (not Web Credentials).
Under the "Generic Credentials" section, scroll down and look for an entry that looks like:
git:https://github.com
Remove/Delete the Entry:

git config --global credential.https://github.com.useHttpPath true
