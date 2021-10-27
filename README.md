
# IT5007 — Tutorial5 — ZHENG YINJIE

```
cd api
npm install
screen mongod 
screen npm start

mongo issuetracker --eval "db.issues.remove({})"
mongo issuetracker scripts/init.mongo.js

cd ..
cd ui
npm install
npm install --save-dev webpack@4 webpack-cli@3
npx webpack public/App.js --output public/app.bundle.js --mode development
npx webpack --mode production
screen npm start
```
## About Q2 in tutorial5

Please see my script in ui/scripts

How to Use  Monge Commands (After executing command "screen mongod")

Init mongo database(I added 20 customers here so as to add more customers in the beginning)

```
cd api     
mongo issuetracker --eval "db.issues.remove({})"
mongo issuetracker scripts/init.mongo.js
```

CRUD

```
mongo issuetracker --eval "db.issues.remove({})"
node scripts/trymongo.js
```

The result please view my git

My git:

[https://github.com/Yinjie-ZHENG/it5007tu5.git](https://github.com/Yinjie-ZHENG/it5007tu5.git)
