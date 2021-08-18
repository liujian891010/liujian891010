## Commitizen
### 全局安装，命令如下
```shell
npm install -g commitizen cz-conventional-changelog
```

### 查看是否安装成功
```shell
 npm ls -g -depth=0
```

### 全局模式下, 需要 ~/.czrc 配置文件, 为 commitizen 指定 Adapter比如: cz-conventional-changelog (一个符合 Angular团队规范的 preset)
```shell
 echo '{ "path": "cz-conventional-changelog" }' > ~/.czrc
```

### 安装成功后，在对应的git项目中，凡是用到git commit命令，一律改为使用git cz



## commitlint
### 全局安装
```shell
  npm install -g @commitlint/cli @commitlint/config-conventional
```

### 生成配置文件
```shell
  echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js
```

### 你也可以在commitlint.config.js制定提交message规范

```js
"module.exports = {extends: ['@commitlint/config-conventional']}"

module.exports = {
  extends: ['@commitlint/config-conventional'],
  rules: {
    'type-enum': [2, 'always', [
      "feat", "fix", "docs", "style", "refactor", "test", "chore", "revert"
    ]],
    'subject-full-stop': [0, 'never'],
    'subject-case': [0, 'never']
  }
};
```



## Husky

### 项目中，安装husky
```shell
npm install husky
```

### 安装成功后需要在项目的package.json中配置
```js
"husky": {
    "hooks": {
      "commit-msg": "commitlint -e $GIT_PARAMS"
    }
  }
```