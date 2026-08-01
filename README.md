# Picture Book Generator Skill

一套把“故事想法”推进到“可连续出图、可排版、可上架验证”的 Codex 绘本生产 skill。

This Codex skill turns a rough story idea into a structured picture-book MVP: story beats, page plan, character/style bible, page-level image prompts, layout rules, QA checks, and publishing notes.

## 为什么它不只是一个 prompt

大多数绘本生成失败，不是因为一句 prompt 写得不够华丽，而是因为生产链断了：

- 故事没有页间因果，只是一组漂亮插画。
- 主角跨页漂移，衣服、体型、表情和道具都不稳定。
- 正文说到的东西画面里没有，画面里出现的东西正文又没交代。
- 图片模型直接写正文，导致错字、乱码、排版失控。
- 封面、内页、三语文字、KDP 上架描述和 QA 没有连成一套流程。

`picture-book-generator` 解决的是整条链路。它要求 agent 先建立故事节奏、角色连续性、视觉锚点和图文契约，再逐页生成提示词，最后用确定性排版和 QA 清单把书做成可交付的样书。

## What Makes It Different

Most AI storybook workflows fail at the production layer, not the imagination layer.

`picture-book-generator` gives an AI coding agent a full editorial and production workflow:

- story architecture before image generation
- page-by-page narrative causality and page-turn hooks
- character continuity rules for multi-page illustration
- prompt templates that preserve visible evidence and avoid visual drift
- layout rules for Chinese, pinyin, English, and mixed-language pages
- a QA checklist for story coherence, child safety, image/text alignment, and publishing readiness
- optional commercial workflow notes for KDP-style MVP validation

It is designed for people who want a real picture-book pipeline, not a pile of disconnected image prompts.

KDP and other platform guidance is for concept validation and publishing preparation only. Verify current platform specifications, content rights, and final export files before submission.

## Capabilities

- Turn a topic, lesson, short text, or character idea into a picture-book MVP.
- Create a page plan with narrative function, page-turn hook, visual evidence, and text draft.
- Build a character and style bible before image generation.
- Write stable page-level prompts for `image_gen` or another image model.
- Keep visible objects, actions, hands, props, and scene anchors consistent across pages.
- Add layout guidance for no-text illustrations, cover text, pinyin, Chinese, and English.
- Check finished pages for story logic, illustration defects, text errors, and child-appropriate content.
- Extend a book concept into publishing notes, product positioning, and series expansion.

## 适合什么场景

- “帮我做一本儿童绘本”
- “把这个故事拆成 12 页绘本”
- “给我整本绘本的角色圣经和分镜 prompt”
- “保持同一个主角连续出图”
- “做中文版/拼音版/中英双语版绘本页面”
- “做一本可用于 KDP 测试的绘本 MVP”
- “检查这本绘本哪里不连贯、哪里要重出图”

## Repository Structure

```text
picture-book-generator/
  SKILL.md
  agents/
    openai.yaml
  references/
    story-structure.md
    character-continuity.md
    visual-styles.md
    prompt-workflow.md
    layout-and-pinyin.md
    reference-corpus-lessons.md
    story-text-structure-lessons.md
    commercial-publishing-workflow.md
    qa-checklist.md
```

## Installation

Clone this repository into your Codex skills directory:



Restart Codex, then ask:

```text
Use $picture-book-generator to turn my story idea into a 12-page picture-book MVP.
```

## 中文使用方式

安装后可以直接说：

```text
用 $picture-book-generator 把“一个怕黑的小朋友学会检查影子”的故事做成 12 页绘本。
```

这个 skill 会默认先输出故事骨架、角色/风格圣经、逐页计划和提示词。需要出图时，再进入逐页图片生成和排版 QA。

## Design Philosophy

The core idea is simple: picture books are systems.

A good page needs a job. A good spread needs a visual contract. A good character needs repeated anchors. A good book needs rhythm, restraint, escalation, and a final emotional turn.

This skill teaches the agent to treat storybook creation as a repeatable creative pipeline: editorial structure first, generation second, QA always.

## License

MIT. Use it, fork it, adapt it, and build better storybook agents with it.
