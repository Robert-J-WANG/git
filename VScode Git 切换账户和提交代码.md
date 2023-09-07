

## VS code Git 切换账户

### 首先，查看当前的用户名和邮箱：

```text
git config user.name   查看用户  
git config user.email   查看邮箱
```

### 然后，修改用户名和邮箱：

```text
git config --global user.name "username"    修改用户
git config --global user.email "email"     修改邮箱
```

### 修改后，可以在查看一次，确定是否修改成功.

### 这样，就完成了！！！



## VSCODE Upload code to GitHub

### 推送的步骤如下：

### 1、[初始化](https://link.zhihu.com/?target=https%3A//so.csdn.net/so/search%3Fq%3D%E5%88%9D%E5%A7%8B%E5%8C%96%26spm%3D1001.2101.3001.7020) 
#### 把本地文件夹转换成 Git 仓库，在项目根目录生成一个本地仓库（隐藏的.git文件夹）

#### git init

### 2、将修改完的文件提交到本地仓储（.git文件夹）的暂存区

#### 提交单个文件
#### git add 当前文件路径/文件名

#### 将所有文件提交到本地仓储 (注意:点 前面有个空格)的暂存区
#### git add .

#### 查看已经提交到暂存区的文件
#### git ls-files

#### 3、提交到本地仓储的版本区，并给这次修改创建版本快照（40位的hash值）

#### git commit -m "修改内容的说明"

#### 4、指定分支

#### git branch -M master (or main)

### 5、设置好提交地址(提前创建好仓库）

#### git remote add origin [https://github.com/Robert-J-WANG/11](https://link.zhihu.com/?target=https%3A//github.com/chuweiyan/taro.git)(自己预先新建的仓库地址)

### 发现这种写法无法提交

### 删除

#### git remote rm origin

### 重新提交

#### git remote add origin git@github.com/Robert-J-WANG/11

### 5、发布到分支,即远程仓储 

#### git push -u origin master (or main)


## 其他使用场景

### Git 文件 2 种状态：
ü未跟踪：新文件，从未被 Git 管理过
ü已跟踪：Git 已经知道和管理的文件

| **文件状态** | **概念**          | **场景**             |
| ----------- | ----------------- | -------------------- |
| 未跟踪（U）  | 从未被 Git 管理过 | 新文件               |
| 新添加（A）  | 第一次被 Git 暂存 | 之前版本记录无此文件 |
| 未修改（''） | 三个区域统一      | 提交保存后           |
| 已修改（M）  | 工作区内容变化    | 修改了内容产生       |

使用：修改文件，暂存，提交保存记录，如此反复

### 暂存区作用：
#### 暂存区 -> 覆盖 -> 工作区，命令：
#### git restore 目标文件   （注意：完全确认覆盖时使用）

#### 从暂存区移除文件，命令：
#### git rm --cached 目标文件
