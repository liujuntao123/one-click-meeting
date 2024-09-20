# one-click-meeting

腾讯会议一键入会小工具

平时要用腾讯会议，但是腾讯会议的体验非常割裂，要先复制会议码，然后打开腾讯会议粘贴，操作很繁琐。

所以写了个小工具，选中会议码后一键就能入会。

## 下面是简单的使用教程：
1. 安装snip.do。
   直接在微软商店就能安装，免费。
2. 安装“一键入会”的snip.do插件。下面方式二选一。
   1. 直接下载插件文件，地址：。然后直接双击文件就能自动导入进去。
   2. 自己新建一个snip.do插件，然后选择创建script插件。选择powershell。粘贴下面的代码
      ```powershell
        $numbers = $PLAIN_TEXT -replace '\D', ''

        Start-Process "wemeet://page/inmeeting?meeting_code=$numbers"
      ```

## 使用效果
鼠标选中会议码，在弹出的图标里选自一键入会，然后就能自动打开腾讯会议并进入到这个会议里面。
