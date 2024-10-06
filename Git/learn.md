Git
---
<p>Source code management tool (OR) version control tool.</p>
<p>It used to maintain source code.</p>

GitHub
------
<p>It web tool in GitHub only used to create repository for maintain the source code.</p>
<p>(Laptop/Desktop) => to GitHub => push</p>

Using git command line
----------------------
Download git
```
https://git-scm.com/downloads/win
```
Configure git
-------------

```
git config --global user.email "github@gmail.com"
```
```
git config --global user.name "github"
```

Initialize git
--------------

```
git init
```

Check file status
-----------------

```
git status
```
Git Add File One OR More
------------------------

```
git add .
```
Git commit
----------
Your work finished stage or message

```
git commit -m "uploaded text file"
```

Push File Repository
--------------------

```
git remote add origin https://github.com/hariharan241a/note.git
git branch -M main
git push -u origin main
```

Update File push
----------------
```
git add .
git commit -m "Updated files"
git push origin master
```

