---
layout: post
title: "Latest Release of Translator"
date: 2024-09-15
categories: [translation, gradio, huggingface]
---

The latest version of the **English to Kinyarwanda** translator is now available at: [https://huggingface.co/spaces/souvorinkg/english-kinyarwanda](https://huggingface.co/spaces/souvorinkg/english-kinyarwanda).

Previously, the space was frequently going down, so I simplified the hosting using **Gradio Spaces**, which is available as part of HuggingFace. Right now, it supports two-way translation much better than the previous model. The space is free to maintain, which is a huge plus, and it serves as a proof of concept that combining back translation and NMT can beat traditional methods that rely on parallel corpora.

However, this version still has some issues:

- It is **slow**, and inconsistently so, with some requests failing to get any result within 20 seconds.
- On load up, the translation time is too high.
- The translation scales poorly with input size—long sentences and paragraphs cause huge delays.
- The solution doesn’t scale well to **multiple languages**, which would be far more useful than just two languages.

The next major update of the translator will focus on improving the **speed** as much as possible using Gradio. If speed cannot be further improved, I’ll look for alternative hosting platforms.

Stay tuned for updates!
