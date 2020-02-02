# Secret Stopper

Pre and post commit hooks to stop yourself from committing secrets to your git repository.

By default will sanitize any file that has the word 'secrets' in it, or that is in a subdirectory \*/secrets/.

### Usage:

#### Install:
```cp pre-commit .git/hooks/
cp post-commit .git/hooks/```
#### Test:
```cp examples/* test/
git add test/*
git commit```
