# MathJax_Tutorial_CN

完备的LaTeX公式中文手册（MathJax环境下）

## 写给 Contributor

显然，这个手册还没写完。如果你想和我一起写，可以参照下面的步骤：

### 1. Folk 该项目并 Clone 到本地

### 2. 运行`docsify`

- 安装 node.js，添加到 path
- 安装 `docsify-cli` 工具。命令行：
  
  ```bash
  npm i docsify-cli -g
  ```
  
- 运行本地服务器。命令行（在项目目录下）：
  
  ```bash
  docsify serve
  ```

  默认端口 [http://localhost:3000](http://localhost:3000) 。直接编辑 `docs/xx.md` 就能更新网站内容。可以让实时的预览。

`docs` 内文件说明：

- `index.html` 入口文件
- `README.md` 会做为主页内容渲染
- `.nojekyll` 用于阻止 GitHub Pages 会忽略掉下划线开头的文件
- `_sidebar.md` 侧边栏目录
