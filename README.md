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
```
