# BASELINT ts+eslint+prettier+hooks基础配置步骤
## 添加ts
npm i -g typescript
tsc --init
npm install --save-dev typescript awesome-typescript-loader  ts-loader  ts-node-dev 
## ts-node-dev --respawn --transpile-only [file path] 即可启动 
## 添加eslint
npm install eslint --save-dev
eslint --init 选择自己想要的规则
package.json 添加 "fix": "eslint src/* --fix"
新建 .eslintignore 添加不需要检测的文件
## 添加prettier
 npm install --save-dev --save-exact prettier
新建  .prettierignore 添加不需要检测的文件
若同时使用eslint 添加eslint-config-prettier
npm install --save-dev eslint-config-prettier
并将 "prettier" 放在.eslintrc.* extends 
ts 添加 "prettier/@typescript-eslint"
## git hooks
npx mrm lint-staged This will install husky and lint-staged
## lint-staged
https://github.com/okonet/lint-staged#configuration