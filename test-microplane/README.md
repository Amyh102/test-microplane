

This script is intended to be used by `microplane` to generate multiple
migration PRs.

Make sure you have the latest version of `microplane` installed following the
[documentation](https://github.com/Clever/microplane).

```sh
# initialize microplane from GH search
mp init "amyh102/test-microplane"

# OR initialize microplane from a list of repositories
# mp init -f repos.txt

# clone all repositories
mp clone

# make the changes
mp plan -b branch-name -m 'feat: delete target' -d -- sh -c ./script.sh

# push the PRs as drafts
mp push -a REPLACE_ME -b ./push_message.txt -d -l microplane
```
