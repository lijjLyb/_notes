# git忽略文件

## 命令列表

### 文件名

.gitignore

### 注释

行注释: 以`#`开头

## 通用符

通用符`*` 

## 忽略文件

[gitignore](https://github.com/github/gitignore)

## 清理缓存

```bash
git rm -r --cached . 
```

有时候在项目开发过程中，突然心血来潮想把某些目录或文件加入忽略规则，按照上述方法定义后发现并未生效，原因是.gitignore只能忽略那些原来没有被track的文件，如果某些文件已经被纳入了版本管理中，则修改.gitignore是无效的。那么解决方法就是先把本地缓存删除（改变成未track状态），然后再提交：( 先把要忽略的文件加入.gitignore，再执行命令)

 ## 常用文件忽略

```gitignore
#//////////
# project
#//////////

build/
data/

#//////////
# VS Code
#//////////

.vscode

#//////////
# mac
#//////////

.DS_Store

#//////////
# NodeJs
#//////////

node_modules/
```