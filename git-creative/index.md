```bash
#!/bin/sh

repo_name=$1
test -z $repo_name && echo "Repo name required." 1>&2 && exit 1

curl -u anothergithubber https://api.github.com/user/repos -d "{\"name\":\"$repo_name\"}"
```

```bash
mkdir new-repo && cd new-repo
```

```bash
git init
git remote add origin git@github.com:anothergithubber/new-repo.git
```

```bash
touch README.md
git add .
```

```bash
git checkout -b gh-pages
git commit -m "Initial"
```

```bash
git push origin gh-pages
```