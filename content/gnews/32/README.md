###  [:house:返回首頁](https://github.com/ourhimalayas/txt)
---

## 有关GTV视频分享的技巧（二）
` 康州盘古喜马拉雅农场` [轉載自GNews](https://gnews.org/zh-hans/609409/)

作者：康州盘古农场-Lioulun

审核：康州盘古农场-Truemanman

我在之前发过一篇关于GTV视频分享的文章，里面提到过使用手动提取的视频 m3u8 文件的地址进行视频转载，那么今天我们来说说如何仅仅通过视频页面的 url 得到 m3u8 文件的地址。

我们先准备一点数据作为分析依据：

[0]

[https://web.gtv.org/video/id=5fc7025bee9d341c2b4109c1](https://web.gtv.org/video/id=5fc7025bee9d341c2b4109c1)

[https://filegroup.gtv.org//group5/vm3u8/20201202/02/56/5fc7025bee9d341c2b4109c1/hls.m3u8](https://filegroup.gtv.org//group5/vm3u8/20201202/02/56/5fc7025bee9d341c2b4109c1/hls.m3u8)

[1]

[https://web.gtv.org/video/id=5fc660db20c9025a87db75f5](https://web.gtv.org/video/id=5fc660db20c9025a87db75f5)

[https://filegroup.gtv.org//group5/vm3u8/20201201/15/27/5fc660db20c9025a87db75f5/hls.m3u8](https://filegroup.gtv.org//group5/vm3u8/20201201/15/27/5fc660db20c9025a87db75f5/hls.m3u8)

[2]

[https://web.gtv.org/video/id=5fc65c7120c9025a87db741b](https://web.gtv.org/video/id=5fc65c7120c9025a87db741b)

[https://filegroup.gtv.org//group5/vm3u8/20201201/15/08/5fc65c7120c9025a87db741b/hls.m3u8](https://filegroup.gtv.org//group5/vm3u8/20201201/15/08/5fc65c7120c9025a87db741b/hls.m3u8)

以上是三段视频的播放页面的地址以及对应手工获取的 m3u8 文件的 url，下面我们将使用其地址直接推导出 m3u8 文件的 url。

### **第一步 确定常量、变量**

很明显“https://filegroup.gtv.org//group5/vm3u8/“以及“/hls.m3u8“都是固定不变的常量，而中间的部分则为变量，例如：“20201202/02/56/5fc7025bee9d341c2b4109c1”、“20201201/15/27/5fc660db20c9025a87db75f5”。

### **第二步 分析变量**

可以发现变量部分的后段的16进位编码就是视频播放地址的id，例如：“id=**5fc7025bee9d341c2b4109c1**“对应”20201202/02/56/**5fc7025bee9d341c2b4109c1**“。所以可以直接用播放页面的地址得到这个字段。

接下来很明显发现，前部分的内容模式为如下形式：

年月日/小时/分钟

通过对视频上传记录的对照可以发现这个日期时间应该就是视频的最早发布事件，接下来的重点是如何得到该字段信息。

**我这里已经通过比对发现如果将 id 字段的前8个16进位数取出就是一个精度到秒的时间戳，把它转换成UTC时间就得到了视频发布的日期和时间，并能够对应 m3u8 地址的字段。**

公式如下：
![]()![](https://gnews-media-offload.s3.amazonaws.com/wp-content/uploads/2020/12/02041106/%E5%9B%BE%E7%89%8718.png)
### **第三步 代码实现**

import time

​test = ‘https://web.gtv.org/video/id=5fc7025bee9d341c2b4109c1’

​tpl = ‘https://filegroup.gtv.org/group5/vm3u8/{}/hls.m3u8’

​id = test.split(‘id=’)[1]

print(id)

​timestamp = int(id[:8], 16)

print(timestamp)

​utc = time.gmtime(timestamp)

date = f'{utc.tm\_year}{utc.tm\_mon:02}{utc.tm\_mday:02}’

hours = f'{utc.tm\_hour:02}’

minutes = f'{utc.tm\_min:02}’

segment = f'{date}/{hours}/{minutes}/{id}’

print(segment)

​url = tpl.format(segment)

print(url)

输出结果：

5fc7025bee9d341c2b4109c1

1606877787

20201202/02/56/5fc7025bee9d341c2b4109c1

https://filegroup.gtv.org/group5/vm3u8/20201202/02/56/5fc7025bee9d341c2b4109c1/hls.m3u8

需要注意的是由于 GTV 版本的更新所以字段 /group5/ 可能会随着改变，不过一般可以采用连接测试的方式简单确定具体版本，毕竟版本不像日期时间那样频繁变更。



1+
