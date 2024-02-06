# 简介

用于下载斗鱼视频录播以及弹幕，支持订阅，自动下载。

# 安装

`npm install douyu-cli`

该程序依赖于`ffmpeg`，需要手动安装，程序默认会调用环境变量中的`ffmpeg`，如果想自定于或者无法调用，请使用`douyu config set ffmpegBinPath xxxx`手动设置可执行文件地址。

# 使用

```bash
Usage: douyu [options] [command]

斗鱼视频下载命令行

Options:
  -V, --version             output the version number
  -h, --help                display help for command

Commands:
  download [options] [url]  下载视频
  subscribe|sub             订阅
  config                    配置项
  dm [options] <vid>        下载弹幕
  help [command]            display help for command
```

## 下载视频

`douyu download https://v.douyu.com/show/yVY8WwdzNyVvLOz9`

你也可以加上`-d`, `-a` 来下载当前视频的所有分 p，并下载弹幕，弹幕为 b 站兼容格式，你可以使用如 [DanmakuFactory](https://github.com/hihkm/DanmakuFactory) 将弹幕转换为 ass 格式进行后续操作。

如果你正在寻找将录播上传到 B 站的工具，可以尝试一下 [biliLive-tools](https://github.com/renmu123/biliLive-tools)，支持将弹幕转换以及压制到视频中并自动上传。

```bash
Usage: douyu download [options] [url]

下载视频

Options:
  -a, --all      下载所有分p
  -d, --danmaku  下载弹幕
  -r, --rewrite  覆盖已有文件
  -h, --help     display help for command
```

## 订阅

### 添加订阅

`douyu sub add 93589`

### 移除订阅

`douyu sub remove 93589`

### 下载订阅

`douyu sub download`

### 定时任务

`douyu sub server`

你也可以使用定时任务来执行 `douyu sub download` 命令，可以到达相同的效果

## 配置

### 查看配置

`douyu config print`

### 更新配置

`douyu config set xxx xxx`

## 其他

请善用`help`指令

# 赞赏

如果本项目对你有帮助，请我喝瓶快乐水吧，有助于项目更好维护。  
爱发电：[https://afdian.net/a/renmu123](https://afdian.net/a/renmu123)  
你也可以给我的 B 站帐号[充电](https://space.bilibili.com/10995238)

# 开发

node<18 未经过测试

## Install

```bash
$ pnpm install
```

## Development

```bash
$ pnpm run dev
```

## Build

```bash
$ pnpm run build
```

# License

GPLv3
