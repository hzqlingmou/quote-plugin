<div align="center">
  <img src="https://s2.loli.net/2022/06/16/opBDE8Swad5rU3n.png" width="180" height="180" alt="NoneBotPluginLogo">
  <br>
  <p><img src="https://s2.loli.net/2022/06/16/xsVUGRrkbn1ljTD.png" width="240" alt="NoneBotPluginText"></p>
</div>

<div align="center">

# nonebot-plugin-quote

_✨ QQ群聊 语录库 ✨_

🧬 支持OCR识别，关键词搜索 | 一起记录群友的逆天言论吧！🎉

<p align="center">
  <img src="https://img.shields.io/github/license/EtherLeaF/nonebot-plugin-colab-novelai" alt="license">
  <img src="https://img.shields.io/badge/python-3.8+-blue.svg" alt="Python">
  <img src="https://img.shields.io/badge/nonebot-2.0.0r4+-red.svg" alt="NoneBot">
  <a href="https://pypi.org/project/nonebot-plugin-quote/">
      <img src="https://img.shields.io/pypi/v/nonebot-plugin-quote.svg" alt="pypi">
  </a>
</p>
</div>

## 📖 介绍

一款适用于QQ群聊天的语录库插件。

- [x] 上传聊天截图
- [x] 随机投放聊天语录
- [x] 根据关键词投放聊天语录
- [x] 支持白名单内用户删除语录
- [x] 支持为指定语录增删标签
- [x] ~~[批量处理已有聊天截图(测试功能)](https://github.com/RongRongJi/nonebot_plugin_quote/blob/main/batch.md) (版本更新，该功能暂时不可用，等后续更新)~~

你的star是对我最好的支持！

交流QQ群: 580407499

## 🎉 使用

### 上传

以**上传**指令回复图片消息，即可直接将图片上传至语录库中。

<img src="https://github.com/RongRongJi/nonebot_plugin_quote/raw/main/screenshot/upload.jpg" width="40%" />


### 随机发送语录

@机器人，发送**语录**指令，机器人将从语录库中随机挑选一条语录发送。

<img src="https://github.com/RongRongJi/nonebot_plugin_quote/raw/main/screenshot/random.jpg" width="40%" />

### 关键词检索语录

@机器人，发送**语录**+关键词指令，机器人将从语录库中进行查找。若有匹配项，将从匹配项中随机一条发送；若无匹配项，将从整个语录库中随机挑选一条发送。

<img src="https://github.com/RongRongJi/nonebot_plugin_quote/raw/main/screenshot/select.jpg" width="40%" />
<img src="https://github.com/RongRongJi/nonebot_plugin_quote/raw/main/screenshot/non.jpg" width="40%" />

### 删除语录

回复机器人发出的语录，发送**删除**指令，机器人将执行删除操作。（该操作只允许设置的白名单用户进行，如何设置白名单请看下方配置）

<img src="https://github.com/RongRongJi/nonebot_plugin_quote/raw/main/screenshot/delete.jpg" width="40%" />

### 增加/删除标签

回复语录图片，发送**addtag**+标签（addtag后需加空格，可以多个标签，每个标签之间用空格分隔），为指定语录增加额外标签。

回复语录图片，发送**deltag**+标签（deltag后需加空格，可以多个标签，每个标签之间用空格分隔），为指定语录删除不需要的标签。

<img src="https://github.com/RongRongJi/nonebot_plugin_quote/raw/main/screenshot/tag.jpg" width="40%" />

### 指定标签检索语录

@机器人，发送**语录**+#号+标签，将从语录库中对指定标签进行查找。加#号后，将只对#号后的完整的词进行查找；不加#号会进行分词。

<img src="https://github.com/RongRongJi/nonebot_plugin_quote/raw/main/screenshot/usetag.jpg" width="40%" />

### 生成语录式图片

在配置好中文字体路径后，以“命令前缀+**生成**”，回复群内任意一句话，即可生成如下语录体图片，**不录入语录库和本地保存**，支持emoji渲染，推荐使用等宽黑体（例如[更纱黑体](https://github.com/be5invis/Iosevka)）以达到最好效果。

<img src="https://github.com/RongRongJi/nonebot_plugin_quote/raw/main/screenshot/auto_generate.png" width="40%" />

### 上传语录式图片

在配置好中文字体路径后，以“命令前缀+**记录**”，回复群内任意一句话，即可生成如下语录体图片，**录入语录库和本地保存**，支持emoji渲染，推荐使用等宽黑体（例如[更纱黑体](https://github.com/be5invis/Iosevka)）以达到最好效果。

<img src="https://github.com/RongRongJi/nonebot_plugin_quote/raw/main/screenshot/auto_record.jpg" width="40%" />

### 详细命令

默认配置下，@机器人加指令即可。

| 指令 | 需要@ | 范围 | 说明 |
|:-----:|:----:|:------:|:-----------:|
| 回复图片+上传 | 可选 | 群聊 | 上传图片至语录库 |
| 语录 + 关键词(可选) | 可选 | 群聊 | 根据关键词返回一个符合要求的图片, 没有关键词时随机返回 |
| 语录 + #标签 | 可选 | 群聊 | 根据标签返回一个符合要求的图片, 没有关键词时随机返回 |
| 回复机器人 + 删除 | 可选 | 群聊 | 删除该条语录 |
| 语句中包含语录 | 是 | 群聊 | 对如何使用语录进行说明 |
| 回复机器人 + addtag + 标签(addtag和标签之间需要空格)| 可选 | 群聊 | 为该条语录增加额外标签 |
| 回复机器人 + deltag + 标签(deltag和标签之间需要空格)| 可选 | 群聊 | 为该条语录删除指定标签 |
| 回复机器人 + alltag| 可选 | 群聊 | 查看该条语录所有标签 |
| 回复消息+记录 | 否 | 群聊 | 为回复消息生成语录式图片并**记录至语录库**，不能上传自己的语录 |
| 回复消息+生成 | 否 | 群聊 | 为回复消息生成语录式图片，**不在本地存储** |

## 💿 安装

### 下载

1. 通过包管理器安装，可以通过nb，pip，或者poetry等方式安装，以pip为例

```
pip install nonebot-plugin-quote -U
```

2. 手动安装

```
git clone https://github.com/RongRongJi/nonebot_plugin_quote.git
```

3. 使用nb-cli安装

```
nb plugin install nonebot-plugin-quote
```

## ⚙️ 配置

在 nonebot2 项目的 `.env` 文件中添加下表中的必填配置

| 配置项 | 必填 | 默认值 | 说明 |
|:-----:|:----:|:----:|:----:|
| FONT_PATH | 是 | None | 必要的语录中文字体文件路径（若不填，部分功能无法使用） |
| AUTHOR_FONT_PATH | 是 | None | 必要的作者中文字体文件路径（若不填，部分功能无法使用） |
| QUOTE_PATH | 否 | ./data | 可选，默认使用'./data' |
| RECORD_PATH | 否 | 'record.json' | 必要的json文件路径, 示例"/data/record.json" |
| INVERTED_INDEX_PATH | 否 | 'inverted_index.json' | 必要的json文件路径, 示例"/data/inverted_index.json" |
| QUOTE_SUPERUSER | 否 | 空字典 | 白名单字典(分群) |
| GLOBAL_SUPERUSER | 否 | 空数组 | 全局管理员(可以删除每个群的语录) |
| QUOTE_NEEDAT | 否 | True | 是否需要at机器人(开启上传通道必须at) |
| QUOTE_STARTCMD | 否 | '' | 增加指令前缀 |

`RECORD_PATH`和`INVERTED_INDEX_PATH`只需要配置，无需创建文件；若不配置`RECORD_PATH`和`INVERTED_INDEX_PATH`，将会自动在项目根目录下创建两个json文件。

`QUOTE_SUPERUSER`的示例如下:

```json
{"群号1":["语录管理员qq号","语录管理员qq号"],"群号2":["语录管理员qq号"]}
```

`GLOBAL_SUPERUSER`的示例如下:

```json
["全局管理员qq号"]
```

**完整的`.env`配置可以参考以下内容**

```
 # linux环境下路径
RECORD_PATH=/home/your_name/your_path/record.json      
INVERTED_INDEX_PATH=/home/your_name/your_path/inverted_index.json
FONT_PATH=/home/your_name/your_path/font.ttf
AUTHOR_FONT_PATH=/home/your_name/your_path/author_font.ttf 

# Windows环境下路径
RECORD_PATH=D:\your_path\record.json       
INVERTED_INDEX_PATH=D:\your_path\inverted_index.json
FONT_PATH=D:\your_path\font.ttf
AUTHOR_FONT_PATH=D:\your_path\author_font.ttf

QUOTE_PATH='./data'
QUOTE_SUPERUSER={"12345":["123456"],"54321":["123456","654321"]}
GLOBAL_SUPERUSER=["6666666"]
QUOTE_NEEDAT=True
QUOTE_STARTCMD=""
```

随后，在项目的`pyproject.toml`或`bot.py`中加上如下代码，加载插件（根据版本而定）

`pyproject.toml`中添加

```
# pip install的填这个
plugins = ["nonebot_plugin_quote"]

# 手动安装的填这个
plugin_dirs = ["nonebot_plugin_quote"]
```

或

`bot.py`中添加

```
# pip install的填这个
nonebot.load_plugin("nonebot_plugin_quote")

# 手动安装的填这个
nonebot.load_plugins("src/plugins", "nonebot_plugin_quote")
```

## 🎉 鸣谢

- [NoneBot2](https://github.com/nonebot/nonebot2)：本插件使用的开发框架。
- [go-cqhttp](https://github.com/Mrs4s/go-cqhttp)：稳定完善的 CQHTTP 实现。

## 开发者

[![contributors](https://contrib.rocks/image?repo=RongRongJi/nonebot_plugin_quote)](https://github.com/RongRongJi/nonebot_plugin_quote/graphs/contributors)