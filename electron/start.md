#### 安装依赖

1. 确保 node 版本 (14.19.1 - 32)

```bash
node -v
14.19.1
```

2. npm 版本

```bash
npm -v
6.14.16
```

3. 安装 python

```bash
python
2.7.15 -32
```

4. 安装 windows-build-tools

```bash
npm install --vs2017 -g windows-build-tools
```

5. 配置 VS 版本

```bash
npm config set msvs_version 2017
```

6. 配置 python 路径

```bash
npm config set python C:\Python27\python.exe
```

7. 安装依赖

```bash
npm i
```

7. 启动项目

```bash
npm run dev
```
