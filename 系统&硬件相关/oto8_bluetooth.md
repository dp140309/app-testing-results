#### 20190529

- patch描述：解决oto8上蓝牙不能使用的问题

- 测试平台：S1笔记本，t45笔记本，Z1-520V一体机，201905290437-oto8-eng.img

- patch内容：

  system/bt

  commit id:409538efc594458e5b826a89b04b1c18b0151f66

  Replace Bluetooth HAL by Intel's implementation. Linaro's implementation is buggy.

  commit id:c4aae0c7481b8355e3d1fb8a33182ba8f88f90a5

  Add back libbt-vendor

- 测试结果

  | 测试点    | 测试内容                                         |s1笔记本|t45笔记本|Z1-520V一体机|
  | -------- | ----------------------------------------------- |--------|--------|--------|
  | 扫描     | 可以扫描到蓝牙设备，扫描结果与手机或其它电脑上的一致    |  通过   |  通过  |  通过   |
  | 配对     | 可以与其它电脑和手机配对                            |  通过  |  通过  |  通过   |
  | 配对     | 可以与WH-1000XM2耳机配对                           |  通过  |  通过  |        |
  | 发送文件  | 可以向其它电脑和手机发送文件 （包括图片和视频）        |  通过  |  通过  |  通过   |
  | 接收文件  | 可以接收其它电脑和手机发送来的文件（包括图片和视频）    |  通过  |  通过  |  通过   |
  | 播音乐    | 可以通过耳机WH-1000XM2播放音乐                     |  通过  |  通过  |        |

  
- 问题列表
   - 1. 蓝牙匹配时，鼠标点击弹出的匹配窗口，窗口会到桌面下方而无法点击 ------------我们目前通过方向键选中匹配按钮
   - 2. 文件管理器的右键发送文件功能不可用 ------------我们目前是通过其它应用的分享功能发送文件
   - 3. openthos电脑接收文件时，通知中心自动弹出的接收文件消息无法点击接收按钮，需要重新打开通知中心才能点击并接收
   - 4. 匹配新设备时，有时需要点击”与新设备匹配”按钮多次才能进入扫描页面 ------------三台电脑均出现过
