# -GitHub基本操作
下载命令 git clone
 上传云端 先存缓存区git add 在本地仓库 git commit -m "简单描述"  在上传 git push
 查看版本号 git log -oneline 回到某个版本 git checkout 版本号-- .()
 xpath //:不考虑当前位置查找 ./：重当前节点开始往下查找 @：选取属性  /:根节点选取 .：当前节点  ..：当前节点的父节点 函数contains :包含某个字符 starts-with:已某个字符开始，取文本/text（）获取节点内容，//text（）获取节点不带标签所有内容；
代码使用xpth from lxml import etree 把文档变成对象，在调用对象方法。1.本地文件tree=etree.parse(文件名)2.网络文件tree=etree.HTML(网页字符串)
 bs a:标签选择器 .dudu：类选择器 #lala：ID选择器 input[name="lala"]：属性选择器 div>p>a：只能是下面一级
jsonpath函数 1.json.dumps():将字典列表转化为json格式的字符串 2.json.loads（）：将json格式字符串转化为python对象3.json.dump（）将字典列表转化为json格式的字符串并且写入文件中4.json.load（）重文件中读取json格式字符串，转化为Python对象 jsonpath简单应用查看：https://www.cnblogs.com/jpfss/p/10973590.html
