1.下载依赖项，输入 npx knex init,useNullAsDefault:true
2.npx knex migrate:make create-lessons-table  
3.在 model 下创建 dbhelper.js 写 add 的异步函数，注意这里一定要是异步函数。  
4.查看 knex 官方文档，写好所有 knex 提供的关于数据库的操作函数（添加数据，查找数据，删除数据，更新数据等），然后作为模块引入到对应 api router 中使用（post/get/getbyid/delete/patch 等）  
5.yarn add dotenv,注意 require('dotenv').config()要放在 index.js 的最顶端,设置环境变量 PORT  
6.设置数据库配置文件 dbConfig.js，不需要在.env 文件中设置生产模式的 DB_ENVIRONMENT 变量，而是在部署时在 heroku 的环境变量中设置  
7.到 knexfile.js 中设置 production 模式下的配置  
8.heroku 通过 package.json 中的"start" script 来启动服务器
