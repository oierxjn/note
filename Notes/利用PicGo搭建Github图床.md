这里利用PicGo上传图片，Github储存图片，jsdelivr加速访问  

# 步骤如下
## 创建Github账户
因为这需要一个储存库来储存照片  
## 创建一个新的储存库
主页右上角点击+号  
![](https://cdn.jsdelivr.net/gh/ptezhub/ptezimg001@main/202320231105190042.png)  
输入储存库名字，记住这个名字，后面要用  
保持公用开启，添加自述文件，最下面完成创建  
![](https://cdn.jsdelivr.net/gh/ptezhub/ptezimg001@main/2023/202311052005749.png)  
## 创建一个访问Github的Token
访问Settings的Profile的Developer settings的Personal access tokens的tokens，网址[https://github.com/settings/tokens](https://github.com/settings/tokens)  
点击 `Generate a personal access token`，即创建一个新的token（需要classic）
### 具体步骤（位置可能随更新变化，推荐直接用上面那个网址）
点击右上角头像，弹出的页面点Settings  
![](https://cdn.jsdelivr.net/gh/ptezhub/ptezimg001@main/2023/202311052048224.png)  
左边找到Developer settings并点击进入  
![](https://cdn.jsdelivr.net/gh/ptezhub/ptezimg001@main/2023/202311052100603.png)  
先在左侧点击Personal access tokens，点击classic的Tokens  
再在右侧点击Generate new token，选择classic创建token  
![](https://cdn.jsdelivr.net/gh/ptezhub/ptezimg001@main/2023/202311052102987.png)  
Notes里面相当于备注  
Expiration设置成No expiration，表示不会过期（如果你不介意过期重新创建的话也可以设置过期时间）  
勾选repo用于上传图片（？）  
![](https://cdn.jsdelivr.net/gh/ptezhub/ptezimg001@main/2023/202311052108362.png)  
划到最下面会有一个确认的按钮，点击创建Token  
![](https://cdn.jsdelivr.net/gh/ptezhub/ptezimg001@main/2023/202311052116874.png)  
记住你的Token，一定要确定你收藏好Token后关掉这个界面！！！  
因为这个Token不会再显示了  
![](https://cdn.jsdelivr.net/gh/ptezhub/ptezimg001@main/2023/202311052113723.png)  
## 下载并安装PicGo
[PicGo官网https://picgo.github.io/PicGo-Doc/](https://picgo.github.io/PicGo-Doc/) （吐槽一下好像还是用github.io，但我喜欢）  
[Github上的PicGo](https://github.com/Molunerfinn/PicGo/)  
### 下载途径
[官方提供的主要下载途径](https://picgo.github.io/PicGo-Doc/zh/guide/#%E4%B8%8B%E8%BD%BD%E5%AE%89%E8%A3%85)  
![](https://cdn.jsdelivr.net/gh/ptezhub/ptezimg001@main/2023/202311052120410.png)  
### 安装
选择合适的版本下载并安装即可  
安装过程中没有需要修改的地方  
## 配置PicGo
点击图床设置：Github设置  
仓库名填刚刚创建储存库记下来的，格式为`[用户名]/[仓库名]`。分支名取决于刚开始创建的主分支名或是已有的分支名，目前github的主分支名默认为`main`。设定Token就是填刚刚创建的Token。存储路径注意要在最后一个文件夹后面加上`/`。设定自定义域名一般用jsdelivr的cdn加速，具体的格式为：`https://cdn.jsdelivr.net/gh/[用户名]/[仓库名]@[分支名]`  
![](https://cdn.jsdelivr.net/gh/ptezhub/ptezimg001@main/2023/202311052126253.png)  

### 可选配置
#### 自定义域名
实际上上文的设定自定义域名也是可选的设置，不过因为国内访问github过慢，不得不借助全球CDN加速。需要注意的是**jsdelivr加速文件的上限为20M**  

`raw.staticdn.net`也可用于加速，具体填进自定义域名中的格式为`https://raw.staticdn.net/[用户名]/[仓库名]/[分支名]`  
似乎它能接受的文件类型较少，[原因在此](https://gitmirror.com/raw.html)  

当然你也可以选择[自建raw加速站点](https://github.com/hunshcn/gh-proxy)
#### PicGo软件配置
建议开启时间戳重命名，适合我这种容易怀旧的。
可以调整显示的图床，如果你有其他图床可用，也可以一起开着。~~但我相信Github白嫖程度最高~~
## 截图后就可以上传图片啦