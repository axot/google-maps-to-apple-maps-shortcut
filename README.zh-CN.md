# Google Maps to Apple Maps Shortcut

一个 iOS 捷径：在 **Google 地图**里搜索地点，然后一键用 **Apple 地图**打开导航。

[安装捷径](https://www.icloud.com/shortcuts/32e44c7daedf4909884206cb362ce4da)

## 适合谁

如果你习惯用 Google 地图找店、看评价、查地点，但开车/CarPlay/Apple Watch/Siri 导航更喜欢 Apple 地图，这个捷径就是为这个流程做的。

## 使用方法

1. 在 iPhone 上打开 Google 地图。
2. 搜索地点或点选地图上的位置。
3. 点分享按钮。
4. 选择 `Apple Map`。
5. Apple 地图会打开到该目的地的驾车路线。

## 已支持的链接类型

- Google Maps 短链接：`https://maps.app.goo.gl/...`
- 商家 / POI 地点卡片。
- 普通地址。
- 掉落的 pin / 指定地点。
- 坐标型目的地。
- 日文、中文等非拉丁字符地点名。
- 展开后包含 `q=地点名`、`q=地址` 或 `q=纬度,经度` 的链接。

## 工作原理

Google 地图通常分享一个短链接：

```text
https://maps.app.goo.gl/...
```

捷径会展开这个链接，提取展开后 URL 里的 `q=` 目的地字段，然后构造 Apple 地图路线 URL：

```text
http://maps.apple.com/?daddr=<destination>&dirflg=d
```

## 隐私

这个捷径在 iPhone 本地运行，不使用自建服务器，不做统计，不上传数据。

## 许可证

MIT License。
