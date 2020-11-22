###  [:house:返回首頁](https://github.com/ourhimalayas/txt)
---

## 有關 GTV 視頻分享的小技巧
` 康州喜马拉雅农场` [轉載自GNews](https://gnews.org/zh-hans/580731/)

![]()![](https://gnews-media-offload.s3.amazonaws.com/wp-content/uploads/2020/10/24064746/WhatsApp-Image-2020-10-24-at-15.08.49.jpeg)
作者：康州农场战友

目前我發現在 GTV 上還不能像 Youtube 那樣使用嵌入分享將視頻的 HTML 播放代碼插入到網站。在 Youtbue 當中我們如果點擊分享按鈕，它會跳出一個選擇界面，讓你可以使用裡面的embed代碼，將視頻嵌入到自己的 HTML 頁面，方便一些視頻博主將自己的 Youtube 視頻搬運到個人網站或團隊頻道。

雖然目前 GTV 並不支持這項便捷的操作，但是相信不久後 GTV 也會通過版本更新來增添這項便捷的功能。不過，雖然現階段 GTV 不能提供到這個功能，但這並不代表我們就完全沒有辦法將 GTV 當中的視頻嵌入到自己的網頁當中。

最最簡單粗暴的方式就是將 GTV 當中的視頻進行下載然後經過轉碼後拿去分享。我們可以使用一些支持下載 HLS 視頻的視頻下載插件將 GTV 視頻下載然後傳播。通過閱讀 GTV 視頻的 hls.m3u8 文件內容，根據字段CODECS=”avc1.4d4028,mp4a.40.2″我們應該是可以將下載下來的文件的擴展名.ts修改為.mp4然後進行播放「電腦端可能只有Windows用戶需要修改擴展名才能播放」。雖然我們可以將下載的視頻文件上傳到我們自己的網站服務器然後進行轉載，但是這樣一來我們自己的服務器就必須負責極大的文件存儲以及讀取的工作，而我們自己的服務器並不是 GTV 這種專業的視頻播放平台，通常來說是不具備那麼強大的存儲和讀取能力的。為此我們不能將視頻直接下載到我們的服務器進行轉載。

不過好在通過觀察 GTV 平台播放視頻時的 Network資源「一般瀏覽器右鍵點Inspect可以找到」 ，我們發現可以手動找到 hls.m3u8 文件。這樣一來我們就可以通過一些開源的 hls 播放器來進行轉載播放了。

我們的第一個步驟是進入 GTV 視頻播放頁面找到 hls.m3u8 文件。
![]()![](https://gnews-media-offload.s3.amazonaws.com/wp-content/uploads/2020/11/22033949/2020-11-21-15-51-48.png)
在找到 hls.m3u8 文件後我們就可以通過 hls.js 視頻播放器開發庫來完成我們的網頁嵌入視頻播放代碼了。
![]()![](https://gnews-media-offload.s3.amazonaws.com/wp-content/uploads/2020/11/22041328/%E6%88%AA%E5%B1%8F2020-11-22-17.11.57.png)
上述代碼中`id="video"` 是指定 Video 標籤的 ID，這需要於 `var video = document.getElementById('video');`的內容統一，這段示例中是 video ；width=”640″ 指定視頻播放器顯示在頁面中的寬度； `var video_src ="GTV`中 hls.m3u8 文件的網絡地址”; 用於指定視頻路徑；src=”https://cdn.jsdelivr.net/npm/[email protected]” 是播放器依賴庫 hls.js ，必須寫上。

下面我們用一個簡單的頁面來測試播放。這裡為了演示，我們可以先構建一個簡單的網頁，然後將上述代碼插入到我們網頁的某個位置當中，然後啟動服務器進行查看。

首先我們構建如下網頁代碼，並將我們的 GTV 播放器代碼嵌入其中
![]()![](https://gnews-media-offload.s3.amazonaws.com/wp-content/uploads/2020/11/22041531/%E6%88%AA%E5%B1%8F2020-11-22-17.14.47.png)![]()![](https://gnews-media-offload.s3.amazonaws.com/wp-content/uploads/2020/11/22041540/%E6%88%AA%E5%B1%8F2020-11-22-17.15.09.png)
將以上代碼保存為 .html 文件後，我們就可以用瀏覽器將其打開了。
![]()![](https://gnews-media-offload.s3.amazonaws.com/wp-content/uploads/2020/11/22033957/2020-11-22-01-39-51.png)
在完成網頁嵌入操作後，我們還可以進行下一步「未來預期」的優化，我們很容易發現 hls.m3u8 文件的地址其實是有章可循的，以如下 URL 為例進行解說：

https://filegroup.gtv.org/group4/vm3u8/20201120/15/23/5fb7df8bb2a6d1532783e3d6/hls.m3u8

頭部分 https://filegroup.gtv.org/group4/vm3u8/ 以及末尾文件名 hls.m3u8 都是固定字段，其中的「5fb7df8bb2a6d1532783e3d6」序列為視頻ID，我們打開 GTV 網頁進入視頻播放頁面就可以看到瀏覽器地址欄上的視頻ID。20201120/15/23 則明顯是發布日期和時間。

有了視頻播放頁面的地址就可以得到視頻ID，如果能進一步通過播放頁面得到發布日期和時間「這個似乎目前沒有辦法簡單得到」，我們就可以直接拼接出 hls.m3u8 的文就地址而無需在瀏覽器中進行檢索。

不過由於目前我還沒有琢磨出通過播放地址直接獲取發布日期時間的方法所以現階段我也只能手工得到 hls.m3u8 文件來進行嵌入。

0
