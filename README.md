# bfg-sandbox

## セットアップ

```sh
brew update
brew install bfg
```

## 実行前

```sh
.
├── README.md
└── password.txt
```

## 実行後

```sh
.
└── README.md
```

## 使い方

```sh
$ pwd
/Users/rm/dev/bfg-sandbox

$ cd ..

$ pwd
/Users/rm/dev

$ ls
bfg-sandbox

$ git clone https://github.com/rema424/bfg-sandbox.git bfg-sandbox-mirror

$ ls
bfg-sandbox   bfg-sandbox-mirror

$ cd bfg-sandbox-mirror

$ pwd
/Users/rm/dev/bfg-sandbox-mirror

$ bfg --delete-files password.txt

Using repo : /Users/rm/dev/bfg-sandbox-mirror/.git

Found 2 objects to protect
Found 4 commit-pointing refs : HEAD, refs/heads/master, refs/remotes/origin/HEAD, refs/remotes/origin/master

Protected commits
-----------------

These are your protected commits, and so their contents will NOT be altered:

 * commit 267ae17e (protected by 'HEAD')

Cleaning
--------

Found 1 commits
Cleaning commits:       100% (1/1)
Cleaning commits completed in 40 ms.

BFG aborting: No refs to update - no dirty commits found??



--
You can rewrite history in Git - don\'t let Trump do it for real!
Trump\'s administration has lied consistently, to make people give up on ever
being told the truth. Don\'t give up: https://github.com/bkeepers/stop-trump
--

$ git reflog expire --expire=now --all && git gc --prune=now --aggressive
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), done.
Total 3 (delta 0), reused 0 (delta 0)

$ git push
```
