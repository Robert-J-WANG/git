

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



## VSCODE Upload code to github

### 推送的步骤如下：

### 1、[初始化](https://link.zhihu.com/?target=https%3A//so.csdn.net/so/search%3Fq%3D%E5%88%9D%E5%A7%8B%E5%8C%96%26spm%3D1001.2101.3001.7020) 输入下面的代码 在项目根目录生成一个隐藏的.git文件夹

#### git init

### 2、将所有文件提交到本地仓储 (注意:点 前面有个空格)

#### git add .

#### 3、提交到分支

#### git commit -m "update"

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

