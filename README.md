
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

The result is shown below:(Or you can view mongo_result.txt)
```
root@1fc2174f15b7:/home/tu5/pro-mern-stack-2/ui# cd ..
root@1fc2174f15b7:/home/tu5/pro-mern-stack-2# cd api
root@1fc2174f15b7:/home/tu5/pro-mern-stack-2/api# ls
about.js        db.js            issue.js      package-lock.json  sample.env      scripts  
api_handler.js  graphql_date.js  node_modules  package.json       schema.graphql  server.js
root@1fc2174f15b7:/home/tu5/pro-mern-stack-2/api# mongo issuetracker --eval "db.issues.remove({})"
MongoDB shell version v4.4.10
connecting to: mongodb://127.0.0.1:27017/issuetracker?compressors=disabled&gssapiServiceName=mongodb
Implicit session: session { "id" : UUID("c7da51ee-2eeb-427d-a7fa-675c0cf199c8") }
MongoDB server version: 4.4.10
WriteResult({ "nRemoved" : 25 })
root@1fc2174f15b7:/home/tu5/pro-mern-stack-2/api# node scripts/trymongo.js                        

-------------------- testWithCallbacks -------------------------
(node:684) [MONGODB DRIVER] Warning: Current Server Discovery and Monitoring engine is deprecated, and will be removed in a future version. To use the new Server Discover and Monitoring engine, pass option { useUnifiedTopology: true } to the MongoClient constructor.
Connected to MongoDB URL mongodb://localhost/issuetracker
Result of find:
 [ { _id: 61797eabff212002ace887f7,
    id: 2,
    name: 'Xaogoo',
    phone: '43962200',
    timestamp: 2021-10-27T16:30:35.100Z } ]
Result of find:
 []
```
## About Q6 in tutorial5
As required in Tutorial 5, I am using a separate UI/API server, use port 5000 for API server and port 3000 for UI server.
## Please DO email me if my repo cannot work, I can send you my docker image which can work stable!
My git:

[https://github.com/Yinjie-ZHENG/it5007tu5.git](https://github.com/Yinjie-ZHENG/it5007tu5.git)
