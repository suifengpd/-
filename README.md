# -GitHub基本操作
下载命令 git clone
 上传云端 先存缓存区git add 在本地仓库 git commit -m "简单描述"  在上传 git push
 查看版本号 git log -oneline 回到某个版本 git checkout 版本号-- .()
# xpath //:不考虑当前位置查找 ./：重当前节点开始往下查找 @：选取属性  /:根节点选取 .：当前节点  ..：当前节点的父节点 函数contains :包含某个字符 starts-with:已某个字符开始，取文本/text（）获取节点内容，//text（）获取节点不带标签所有内容； 先生成对象，在调用方法；tree=etree.parse(文件名本地) tree=etree.HTML(网页字符串)
代码使用xpth from lxml import etree 把文档变成对象，在调用对象方法。1.本地文件tree=etree.parse(文件名)2.网络文件tree=etree.HTML(网页字符串)
# bs a:标签选择器 .dudu：类选择器 #lala：ID选择器 input[name="lala"]：属性选择器 div>p>a：只能是下面一级
# jsonpath函数 1.json.dumps():将字典列表转化为json格式的字符串 2.json.loads（）：将json格式字符串转化为python对象3.json.dump（）将字典列表转化为json格式的字符串并且写入文件中4.json.load（）重文件中读取json格式字符串，转化为Python对象 jsonpath简单应用查看：https://www.cnblogs.com/jpfss/p/10973590.html
# selenium 谷歌驱动下载地址http://chromedriver.storage.googleapis.com/index.html 谷歌驱动与谷歌浏览器映射表 https://blog.csdn.net/zhu940923/article/details/81129122
方法：find_element_by_id:根据id查找 find_elements_by_name:根据name查找 find_element_by_xpath:根据xpath查找  find_elements_by_tag_name:根据标签名查找  find_elements_by_class_name:根据class查找  find_elements_by_css_name:根据选择器查找  find_elements_by_link_text
# requests 三方库 r.text 字符串查看响应 r.content字节类型查看响应 r.encoding 查看或者设置编码  r.status_code 查看状态码 r.headers 查看响应头部 r.url 查看响应路径 r.json()查看json数据
# 线程 面向过程 t=threading.Thread(target=XXX(线程启动的函数),name=XX（线程的名字），args=()参数传递 t.start()线程启动 t.join()让主线程等待子线程结束 面向对象 自己新建class
线程变量为全局变量 需要使用锁 创建锁 suo=threading.Lock() 上锁suo.acquire() 释放锁suo.release() 队列 import queue from Queue 创建队列 q=Queue()放入数据q.put() 获取 q.get()
q.empty()队列是否为空 q.qsize() 队列长度 q.full()队列是否满
