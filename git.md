Find replace:

```sh
# http://stackoverflow.com/a/21685766
git grep -lz 'subdomainA.example.com' | xargs -0 perl -i'' -pE "s/subdomainA.example.com/subdomainB.example.com/g"
```

## Commit history for a user

```
git log master --author="$(git config user.name)" --since=57.weeks --pretty=format:"%h - %an, %ad : %s"
```
