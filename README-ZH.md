# Flutter仿微信相机资源选择器

[![pub package](https://img.shields.io/pub/v/wechat_camera_picker?logo=dart&label=%E7%A8%B3%E5%AE%9A%E7%89%88&style=flat-square)](https://pub.dev/packages/wechat_camera_picker)
[![pub package](https://img.shields.io/pub/v/wechat_camera_picker?color=42a012&include_prereleases&label=%E5%BC%80%E5%8F%91%E7%89%88&logo=dart&style=flat-square)](https://pub.dev/packages/wechat_camera_picker)
[![GitHub stars](https://img.shields.io/github/stars/fluttercandies/flutter_wechat_camera_picker?logo=github&style=flat-square)](https://github.com/fluttercandies/flutter_wechat_camera_picker/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/fluttercandies/flutter_wechat_camera_picker?logo=github&style=flat-square)](https://github.com/fluttercandies/flutter_wechat_camera_picker/network)
[![Build status](https://img.shields.io/github/workflow/status/fluttercandies/flutter_wechat_camera_picker/Build%20test?label=%E7%8A%B6%E6%80%81&logo=github&style=flat-square)](https://github.com/fluttercandies/flutter_wechat_camera_picker/actions?query=workflow%3A%22Build+test%22)
[![CodeFactor](https://img.shields.io/codefactor/grade/github/fluttercandies/flutter_wechat_camera_picker?logo=codefactor&label=%E4%BB%A3%E7%A0%81%E8%B4%A8%E9%87%8F&logoColor=%23ffffff&style=flat-square)](https://www.codefactor.io/repository/github/fluttercandies/flutter_wechat_camera_picker)
[![GitHub license](https://img.shields.io/github/license/fluttercandies/flutter_wechat_camera_picker?style=flat-square&label=%E5%8D%8F%E8%AE%AE)](https://github.com/fluttercandies/flutter_wechat_camera_picker/blob/master/LICENSE)
<a target="_blank" href="https://jq.qq.com/?_wv=1027&k=5bcc0gy"><img border="0" src="https://pub.idqqimg.com/wpa/images/group.png" alt="FlutterCandies" title="FlutterCandies"></a>

Language: [English](README.md) | 中文简体

[**仿微信资源选择器**](https://pub.dev/packages/wechat_assets_picker)的扩展。基于 `camera` 实现相机相关功能， `photo_manager` 实现资源相关内容。

## 目录 🗂

* [特性](#特性-)
* [截图](#截图-)
* [准备工作](#准备工作-)
* [使用方法](#使用方法-)

## 特性 ✨

- [x] 💚 99%的微信风格
- [x] 📷 支持拍照
- [x] 🎥 支持录像
  - [x] ⏱ 支持限制录像时间


## 截图  📸

| ![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ggtt6yrdqej30u01t017w.jpg) | ![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ggtt6yh3x4j30u01t0wuo.jpg) |
|-----------------|------------------|
| ![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ggtt6z1h7xj30u01t01kx.jpg) | ![](https://tva1.sinaimg.cn/large/007S8ZIlgy1ggtt6zarvhj30u01t0x5f.jpg) |

## 准备工作 🍭

参考: [wechat_assets_picker#准备工作](https://github.com/fluttercandies/flutter_wechat_assets_picker/blob/master/README-ZH.md#preparing-for-use-)

## 使用方法 📖

| 参数名                     | 类型                       | 描述                                          | 默认值                          |
| ------------------------ | -------------------------- | ---------------------------------------------------- | -------------------------------------- |
| isAllowRecording         | `bool`                     | 选择器是否可以录像                 | `false`                                |
| isOnlyAllowRecording | `bool` | 选择器是否仅可以录像。只在 `isAllowRecording`  为 `true` 时有效。 | `false` |
| maximumRecordingDuration | `Duration`                 | 录制视频最长时长 | `const Duration(seconds: 15)`          |
| theme                    | `ThemeData`                | 选择器的主题                           | `CameraPicker.themeData(C.themeColor)` |
| textDelegate             | `CameraPickerTextDelegate` | 控制部件中的文字实现       | `DefaultCameraPickerTextDelegate`      |

### 简单的使用方法

```dart
final AssetEntity entity = await CameraPicker.pickFromCamera(context);
```

在选择器唤起后，并且 `isAllowRecording` 为 `true`，点击拍摄按钮以拍照，长按拍摄按钮以录像。