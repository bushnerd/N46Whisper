# N46Whisper

Language : [English](./README.md)  | 简体中文

N46Whisper 是基于 Google Colab 的应用。开发初衷旨在提高乃木坂46（以及坂道系）字幕组的工作效率。但本应用亦适于所有日语视频的字幕制作。

此应用基于AI语音识别模型 [Whisper](https://github.com/openai/whisper)

应用输出文件为ass格式，内置指定字幕组的字幕格式，可直接导入 [Aegisub](https://github.com/Aegisub/Aegisub) 进行后续翻译及时间轴校正。

## 更新：

2023.3.12:
* 添加chatGPT翻译并生成双语字幕功能.
* 修订文档以及其它一些优化。

2023.01.26：
* 更新脚本以反映近期Whisper的更新。

2022.12.31：
* 添加了允许用户从挂载的谷歌云盘中直接选择要转换的文件的功能。本地上传文件的选项仍然保留。
* 修订文档以及其它一些优化。

## 如何使用
* [点击这里](https://colab.research.google.com/github/Ayanaminn/N46Whisper/blob/main/N46Whisper.ipynb) 在Google Colab中打开应用.
* 上传要识别的文件并运行应用
* 识别完成后ass文件会自动下载到本地.

## AI翻译
应用现在可以使用AI翻译工具对转录的文本进行逐行翻译。

目前支持`chatGPT` 并默认翻译成中文 `zh-CN`.

翻译后的文本将于原文合并在一行，以 `/N`分割，生成双语对照字幕。

例如: 

![QQ截图20230312155700](https://user-images.githubusercontent.com/49441654/224525469-18a43cbc-33b9-4b2f-b7ca-7ae0c1865b17.png)

双语字幕效果为:

![QQ截图20230312160015](https://user-images.githubusercontent.com/49441654/224525526-51e2123c-6e1c-427c-8d67-9ccd4a7e6630.png)

用户需要自己的OpenAI API Key来使用翻译功能. 要生成免费的Key，进入自己账户设定 https://platform.openai.com/account/api-keys

请注意免费Key有用量限制，翻译速度会较慢。用户可以自己选择付费方案。

## 支持
根据我们使用若干视频的测试结果，输出字幕的识别准确率可以达到90%以上，这无疑能极大地节省听译及打轴所需的人手和时间。但本应用的目标并非产生完美的字幕文件， 而旨在于搭建并提供一个简单且自动化的使用平台。Whisper模型有其本身的应用场景限制，例如视频中出现明显地背景音，长时间空白和多人对话，都可能影响识别准确度。您可以阅读官方文档及讨论区来进一步了解如何使用Whisper以及常见问题。

但如果您有针对应用本身或字幕制作相关的建议、需求、或问题，欢迎随时提出issue或者[联系我们](mailto:admin@ikedateresa.cc)
