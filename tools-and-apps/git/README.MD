# git (my notes)

## LF
git config --global core.autocrlf false<br>
https://stackoverflow.com/questions/71995658/how-to-stop-github-desktop-from-changing-my-line-endings<br>
REMEMBER TO ALSO CONFIGURE WINDOWS TO ENSURE THAT GITHUB DESKTOP TO USE IT<br>

To list configurations:<br>
git config --global --list --show-origin<br>
https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/The-global-Git-config-files-key-settings-and-usages#:~:text=To%20see%20all%20of%20properties,gitconfig%20file's%20location

https://stackoverflow.com/questions/2517190/how-do-i-force-git-to-use-lf-instead-of-crlf-under-window<br>

https://docs.github.com/en/get-started/getting-started-with-git/configuring-git-to-handle-line-endings

## Delete whole commit history
https://blog.avneesh.tech/how-to-delete-all-commit-history-in-github

Create a new branch<br>
```git checkout --orphan new_main```

Add all the files<br>
```git add .```

Commit the changes<br>
```git commit -m "initial"```

Delete the main/master branch<br>
```git branch -D main```

Rename the current branch to main<br>
```git branch -m main```

Finally, force update your repository<br>
```git push -f origin main```

## Delete all local branches

```
git remote prune origin
git fetch --prune && git branch -vv | grep ': gone]' | awk '{print $1}' | xargs git branch -D
```

## Several github accounts (Windows)
Open Credential Manager:<br>
Press Windows Key + S (or click the Start button and start typing).<br>
Type "Credential Manager" and open the application.<br>
Go to Windows Credentials:<br>
In the Credential Manager window, make sure you click on the "Windows Credentials" tab (not Web Credentials).<br>
Under the "Generic Credentials" section, scroll down and look for an entry that looks like:<br>
git:https://github.com<br>
Remove/Delete the Entry:<br>
git config --global credential.https://github.com.useHttpPath true<br>

## Exclude file (Linux repo with invalid Windows file name)
```
mkdir <repo>
cd <repo>
git init
git remote add origin https://github.com/<organization>/<repo>.git
git config core.sparseCheckout true
echo "/*" > .git/info/sparse-checkout
echo '!/files/etc-avahi-avahi\x2ddaemon.conf.mount' >> .git/info/sparse-checkout
git config core.protectNTFS false
git pull origin main
```
