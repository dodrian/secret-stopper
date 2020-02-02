# Secret Stopper

Pre and post commit hooks to stop yourself from committing secrets to your git repository.

By default will sanitize any file that has the word 'secrets' in it, or that is in a subdirectory \*/secrets/.

### Usage:

#### Install:
```bash
cp pre-commit /path/to/repo/.git/hooks/
cp post-commit /path/to/repo/.git/hooks/
```
#### Test locally:
```bash
git clone https://github.com/dodrian/secret-stopper.git
cd secret-stopper
cp pre-commit post-commit .git/hooks/
cp -r examples/* test/
git add test
git commit -m "Testing secret-stopper"
```
After commit, the secrets file will show as modified.  `git diff test/secrets.env` shows that the file committed has been stripped of secrets.
