```bash
create-react-app upgraded-goggles
```

```bash
cd upgraded-goggles
```

```json
// package.json
{
  "name": "upgraded-goggles",
  "version": "0.1.0",
  "private": true,
  "homepage": "https://anothergithubber.github.io/upgraded-goggles",
```

```bash
npm install --save-dev gh-pages
```

```json
// package.json
  "scripts": {
    ...
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build"
  }
```

```bash
git init
git add .
git commit -m "First commit"
git remote add origin https://github.com/anothergithubber/upgraded-goggles.git
```

```bash
npm run deploy
```

[app](https://anothergithubber.github.io/upgraded-goggles/) [repo](https://github.com/anothergithubber/upgraded-goggles) 
