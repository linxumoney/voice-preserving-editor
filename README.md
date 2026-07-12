# Voice Preserving Editor：改掉 AI 腔，但别把作者本人也改没了

很多“去 AI 味”工具只是把一批词换成另一批词，最后文章更口语，却不像原作者。真正的编辑应该保留事实、立场和节奏，只处理模板感、空话和不自然的组织方式。

`voice-preserving-editor` 是一个面向中文和英文写作的开源 Agent Skill。它先建立作者声音基线，再进行最小必要改写，并解释最影响阅读的编辑决定。

## 使用示例

```text
用 $voice-preserving-editor 编辑这篇文章。
这是我以前写的一段文字，请保持我的句子节奏和直接程度。
不要增加新观点，也不要为了口语化删掉事实。
```

## 它不会做什么

- 不承诺绕过 AI 检测器
- 不伪装作者身份或写作过程
- 不自动增加个人经历、情绪和观点
- 不为了“更像人”故意加入错误

## 安装

```bash
cp -R skills/voice-preserving-editor ~/.codex/skills/
```

## 方法参考

本项目独立实现。AI 写作模式识别问题域参考了 [blader/humanizer](https://github.com/blader/humanizer)，该项目采用 MIT License。本项目没有复制其模式清单、示例、章节结构或原文表达，核心流程改为“声音基线 + 编辑预算 + 事实锁定”。

## License

MIT License。
