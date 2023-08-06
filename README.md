# utils
these are set of utilities to speed up recurring tasks

### After cloning a repo, fetch all the branches 

```
git config --global alias.fetchall '!git fetch --all && for branch in $(git branch -r | grep -v '\''\->'\'' | sed '\''s/origin\///'\''); do if ! git show-ref --quiet refs/heads/"$branch"; then git checkout --track -b "$branch" "origin/$branch"; fi; done'
```
```
git fetchall
```


