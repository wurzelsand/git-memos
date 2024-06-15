# Git-memos

* Create a new repository (e.g. "git-memos"). Check the "Create README" box.

* ```gh repo clone wurzelsand/git-memos``` (no `.git` as extension!)

* Make a note of an existing token or create a new one (profile picture at the top right and select Settings/Developer Settings/Personal access tokens/Tokens). It looks something like this: *ghp_Qu8abUO6axHkWQu7WeQoRX7EibwUxe317Q1TX*

* ```cd git-memos```

* ```git remote set-url origin https://ghp_Qu8abUO6axHkWQu7WeQoRX7EibwUxe317Q1TX@github.com/wurzelsand/git-memos```

* ```git pull```
* Make any changes in your local repository.
* ```git add --all```
* ```git commit -m "okay"```
* ```git push```

But now I received the following error message after `git pull` applied to an older repository:

```
fatal: unable to update url base from redirection:
...
```

What helped, although I don't know  how:

* I was logged in with token:

    ```
    gh auth login
    ```

    Choosed https and token login.

* Edit origin: `git config --edit` and/or set remote **with** `.git` as extension and **whithout** token:

    ```
    git remote set-url origin https://github.com/wurzelsand/flutter-memos.wiki.git
    ```


