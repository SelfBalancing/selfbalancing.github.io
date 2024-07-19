

![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E4%B8%BB%E9%A1%B5%E5%8A%A0%E4%B8%80%E4%B8%AA%E6%92%AD%E6%94%BE%E5%99%A8.png)
## 前言

前几天有群友询问能否在Components组件中显示Mp4文件，这个其实很好解决，Obsidian是可以显示大部分格式的视频文件的，只需搭配`![[视频.mp4]]`的语法就能显示，这时再搭配Components组件中的Markdown组件，即可完成视频文件的显示，这样就配置好了一个播放器组件。
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E8%AF%AD%E6%B3%95%E7%A4%BA%E4%BE%8B.png)
除了视频，音乐也能通过这样的方式组合成音乐播放器组件。
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E9%9F%B3%E4%B9%90%E6%92%AD%E6%94%BE%E5%99%A8.png)
可以将播放器组件放置于主页，和其他组件一起呈现，每次启动Obsidian后可以播放音乐。也可以将播放器放置于侧边，写累了可以点击放一首歌曲。
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E4%BE%A7%E8%BE%B9%E6%92%AD%E6%94%BE%E5%99%A8.png)
思路打开，这个播放器组件除了放本地的视频和音频，还能不能再来点花样，播放一下在线视频和自己的歌单音乐？
经过我的一番研究，以及在`@!惊佬`的帮助下，我整合出了几个有意思的播放器组件，更加美观，更加强大。

展示的播放器组件已经整合成一个组合组件,公众号后台回复`播放器`即可获得下载地址。![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E7%BB%84%E5%90%88%E6%92%AD%E6%94%BE%E5%99%A8.png)
## 效果展示


### 视频播放器
#### 功能更强的本地播放器组件
支持调整音量与播放速度等功能


![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240717110433.png)



#### 在线视频播放器
可以直接嵌入在线视频，不用将视频保存至本地了。

![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E6%94%AF%E6%8C%81%E5%9C%A8%E7%BA%BF%E8%A7%86%E9%A2%91.png)


### 音频播放器

#### 单曲网易云播放器
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E4%B8%8D%E5%B8%A6%E6%AD%8C%E5%8D%95%E7%9A%84%E6%99%AE%E9%80%9A%E6%92%AD%E6%94%BE%E5%99%A8.png)
#### 带歌单的网易云播放器
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E9%9F%B3%E4%B9%90%E6%92%AD%E6%94%BE%E5%99%A81.png)
#### 随机在线播放器

![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E6%92%AD%E6%94%BE%E5%99%A81.gif)

## 配置教程


### 视频播放器组件
#### 功能更强的本地播放器组件

在Obsidian中增强一下默认播放器的功能，图一是默认播放器。
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E8%AF%AD%E6%B3%95%E7%A4%BA%E4%BE%8B.png)

图二是增强的播放器
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240717110433.png)

通过`Media Extended`插件对默认的播放器进行了增强，下载地址如下
```
[PKM-er/media-extended: enhanced media(video/audio) playback for obsidian.md (github.com)](https://github.com/PKM-er/media-extended)
```
直接启用插件，即可增强默认播放器
增强本地的视频播放是`Media Extended`功能的一个体现，不过`Media Extended`最强的还是它能够直接在Obsidian中播放在线视频，使得我们可以通过Components配置一个在线视频播放器组件。

#### 在线视频播放器
配置过程十分简易：
1. 打开B站找到相应的视频
2. 复制视频的地址链接
3. 启动Obsidian，创建组件
4. 选择创建Markdown组件，`内容类型`为`文本内容`
5. 在框内填写`![](视频的地址链接)`，括号内填写视频的地址链接

![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/20240717205343.png)


如果你想让播放器组件中视频的画质更高，可以通过`Media Extended`插件的管理界面，登录上自己的账号，可以获得更清晰的画质。
1. 在设置中打开`Media Extended`的管理界面
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E7%99%BB%E5%BD%95%E4%B8%80%E4%B8%8B%E7%BD%91%E7%AB%99.png)
2. 点击`Login`的`Open broswer`打开内置浏览器
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/B%E7%AB%99%E7%99%BB%E5%BD%95%E6%BC%94%E7%A4%BA.png)
3. 在上方框内输入`https://www.bilibili.com`，然后点击头像框进行登录。此时播放器组件将拥有高清画质


### 音乐播放器组件

#### 单曲网易云播放器

单首歌曲的网易云播放器是通过iframe实现的，可以在网易云网页播放界面点击`生成外链播放器`即可获取。


![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E8%8E%B7%E5%BE%97%E5%A4%96%E9%93%BE%E6%92%AD%E6%94%BE%E5%99%A8.png)



![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E9%85%8D%E7%BD%AEiframe.png)

将生成的HTML代码复制至Obsidian中，此时还无法显示播放器
```
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=2158973221&auto=1&height=66"></iframe>
```
需要在`//music.163.com`的前面加上`http:`才能在Obsidian中显示
```
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="http://music.163.com/outchain/player?type=2&id=2158973221&auto=1&height=66"></iframe>
```
简单讲解一下这个代码
1. 如果你想改宽高尺寸的话，修改这里的数字即可：`width=330 height=86 `
2. 目前是默认自动播放，如果要修改为手动播放，修改此处的`1`改为`0`即可：`auto=1`
3. 如果需要修改单曲，修改id后的数字即可：`id=2158973221`
这个id还是比较好获取的，点击音乐分享出去，选择`复制链接`
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E5%88%86%E4%BA%AB%E9%9F%B3%E4%B9%90%E8%8E%B7%E5%8F%96id.png)
`复制链接`的文本中就有对应音乐的id
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E8%8E%B7%E5%8F%96%E7%9A%84id.png)
将此id单独复制出来后，替换掉播放器代码中的id即可

然后将此播放器代码放置于Components的Markdown组件中，即可显示出一个播放器组件。
可能长宽不是特别适配，需要自己修改一下代码中`width=330 height=86 `对应的数字进行调整。



#### 带歌单的网易云播放器

步骤与上面说的差不多，选择歌单后，点击生成外链播放器即可获得歌单的播放器代码，自行进行修改和适配。
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E6%AD%8C%E5%8D%95%E7%9A%84%E6%92%AD%E6%94%BE%E5%99%A8.png)




![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E9%9F%B3%E4%B9%90%E6%92%AD%E6%94%BE%E5%99%A81.png)

这里`@!惊佬`分享了魔改后更好玩的歌单播放器组件，可以在每次启动页面时，从填入的id中随机选择一个歌单进行播放
````
```dataviewjs
let arr = [778413627, 2323555471, 7354648923, 360062344, 5454637196, 2961061456];  // 歌单id数组
let randomIndex = Math.floor(Math.random() * arr.length);  // 生成一个随机索引
let randomElement = arr[randomIndex];  // 使用这个索引从数组中选择一个元素
dv.paragraph(`<iframe title="iframe" src="https://music.163.com/outchain/player?type=0&amp;id=${randomElement}&amp;auto=0&amp;height=240" sandbox="allow-same-origin allow-scripts allow-popups allow-forms" scrolling="no" style="width: 100%; border: 0px; height: 240px;" class="iframe"></iframe>`)
```
````
此段代码可以直接在Markdown组件或Dataviewjs代码中进行部署。

其实网易云音乐的这个外链播放器很强的🥰，不仅能放单曲、歌单，甚至专辑、电台、有声书也能生成外链播放器，步骤都大同小异。
![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E8%BF%98%E8%83%BD%E5%B5%8C%E5%85%A5%E6%9C%89%E5%A3%B0%E4%B9%A6.png)



#### 随机在线播放器

这个就是做的比较好看，缺点就是不能自定义歌单，不过也有几十首歌曲可以选择。
这个组件也放在组合的播放器了，公众号后台回复`播放器`即可获取🥰

![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E6%92%AD%E6%94%BE%E5%99%A81.gif)


今天主要使用的是Markdown组件，后续会持续讲解其他组件的使用教程，最近几期会讲解一下`摘录组件`和其他插件的配合使用，感兴趣的可以关注一下！

![](https://obsidian-1324919814.cos.ap-chengdu.myqcloud.com/%E6%A0%B9%E6%8D%AE%E9%9C%80%E6%B1%82%E8%BF%9B%E8%A1%8C%E9%80%89%E6%8B%A9.png)
