# start_nodejs
Source nodejs with sequelize

# npm install
npm i --save sequelize
npm i --save sequelize-cli

######## CREATE SEQUELIZE ###########
# create file .sequelizerc
const path = require('path');
module.exports = {
  "config": path.resolve('./app/config', 'db-config.json'),
  "models-path": path.resolve('./app/models'),
  "seeders-path": path.resolve('./app/seeders'),
  "migrations-path": path.resolve('./app/migrations')
};
# run folder config, model, migration, seeder
node_modules/.bin/sequelize init

######## CREATE BABEL ###############
# npm babel
npm i --save-dev babel-cli
npm i --save-dev babel-preset-es2015
npm i --save-dev babel-preset-stage-2
# create file .babelrc
{
  "presets": ["es2015"]
}

######## CREATE NODEMON #############
# npm nodemon
npm i --save-dev nodemon
# change script package.json
./node_modules/.bin/nodemon index.js --exec babel-node --presets es2015,stage-2

