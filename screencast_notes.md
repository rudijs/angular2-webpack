Angular2 is more of a platform
- web apps
- mobile apps
- native apps
- desktop apps w/ electron
- Angular2 in web workers
- Angular2 Offline w/ service workers

npm init
npm install --save angular2
npm install --save-dev typescript typings

#from angular.io
tsconfig.json
typings.json

#update tsconfig.json
"module": "commonjs",
"outDir": "build"

./node_modules/.bin/typings install

mkdir -p src/components

create app.component.ts and copy sample from angular.io

#test a typescript build
./node_modules/.bin/tsc

npm i -D webpack webpack-dev-server ts-loader

create webpack.config.js
=> 1.webpack.config.js

create src/main.ts

create src/index.html

node_modules/.bin/webpack

npm i -D rimraf

update package.json with build task

=> npm i -D html-webpack-plugin
=> var HtmlWebpackPlugin = require('html-webpack-plugin');
=>
  plugins: [
    new HtmlWebpackPlugin({ template: 'index.html' })
  ]

npm run build

./node_modules/.bin/webpack-dev-server --inline --hot

update package.json with build task

npm start

# Move inline templates to own file but retain inline feature
template: require('./app.html')

# Add webpack html loader
npm i -D html-loader

update webpack.config.js

npm start

fix console error:
error TS2304: Cannot find name 'require'.

./node_modules/.bin/typings install node --ambient --save

npm start

Review where we're at.

# Pause the recording, build out the app a little beyond just hello world, review updates

npm start