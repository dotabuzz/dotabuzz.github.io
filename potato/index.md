#!/bin/bash

./git-create $1
create-react-app $1 && cd $1

sed -i "/\"private\": true,/a\ \ \"homepage\": \"https://anothergithubber.github.io/$1/\"," package.json

npm install --save-dev gh-pages

sed -i "/\"eject\": \"react-scripts eject\"/a\ \ \ \ \"predeploy\": \"npm run build\",\n    \"deploy\": \"gh-pages -d build\"" package.json

sed -i "s/\"eject\": \"react-scripts eject\"/\"eject\": \"react-scripts eject\",/g" package.json

git init
git add .
git commit -m "First commit"
git remote add origin git@github.com:anothergithubber/$1.git

npm run deploy