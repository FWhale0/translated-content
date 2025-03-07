---
title: 如何带着 SEO 的思维将 MDN 的 Web 文档写的更符合搜索引擎展现
slug: MDN/Contribute/Howto/Write_for_SEO
tags:
  - MDN 内容贡献
  - MDN 搜索优化
  - MDN 搜索引擎优化
  - MDN 文档
  - MDN 的 SEO 优化
  - SEO
  - 搜索引擎优化
translation_of: MDN/Contribute/Howto/Write_for_SEO
---
{{MDNSidebar}}

本指南涵盖了我们对内容的基础要求、推荐和实践参考，以确保搜索引擎可以更好的对我们的内容进行分类和索引，同时确保用户可以轻松地获取到所需的内容。

## 简介

MDN 写作的首要目标是向开发者们阐明和指导开放的 Web 技术，以便他们能够快速找到他们想要的东西，或者为了优化自己的代码而寻找需要的细节，因此我们在 MDN 提供的内容可以被更容易的搜索到就非常重要了。

由于绝大部分读者是通过搜索引擎搜索找到 MDN 的内容的，那么作为作者，我们就要始终记得内容对搜索引擎的友好程度这件事。为了对搜索引擎友好，我们撰写了 SEO 指引的内容以帮助 MDN 的作者和编辑们能够确保 MDN 上的每篇内容的设计、撰写和标记方式都符合 SEO 规范，以获得搜索引擎更好的收录索引和展现。

## 本文档的状态

目前我们刚开始了改进 MDN 文档在搜索引擎优化 ({{Glossary("SEO")}}) 的长期项目的初期阶段。我们最近完成了一系列小规模实验来测试能提升 SEO 的方法，并确定哪些内容能够作为 SEO 指南提供给我们的贡献者们。

我们仍在编辑并更新本文，同时将其他贡献者提供的参考纳入到我们的发现中。

## SEO 要点

The following is a list of things you should check while writing and reviewing content to help ensure that the page and its neighbors will be indexed properly by search engines.

- Make sure the page's contents are [different enough from other pages](/en-US/docs/MDN/Contribute/Howto/Write_for_SEO#Ensure_pages_aren't_too_similar) that search engines don't assume they're about the same thing.

## 避免过于相似的内容页面

Each article should be as unique as possible. Articles that look similar to one another textually will wind up being considered to be about roughly the same thing, even if they aren't. For example, if an interface has the properties `width` and `height`, it's easy for the text to be surprisingly similar, with just a few words swapped out, and using the same example. This makes it hard for search engines to know which is which, and they wind up sharing page rank, resulting in both being harder to find than they ought to be.

Understandably, writers confronted with two related properties like `width` and `height` (or any other set of functionally related features) are tempted to write the article on `width`, then copy that article and paste it into the one on `height`, replacing a few words. Done!

Unfortunately, the result is two pages that, as far as search engines are concerned, may as well be the same thing.

It's important, then, to ensure that every page has its own content. Here are some suggestions to help you accomplish that:

- Consider use cases where there might be more differences than one would think. For instance, in the case of `width` and `height`, perhaps consider ways horizontal space and vertical space are used differently, and provide a discussion about the appropriate concepts. Perhaps you mention the use of width in terms of making room for a sidebar, while using height to handle vertical scrolling or footers or similar. Including information about accessibility issues is a useful and important idea as well.
- Use entirely different examples on each page. Examples in these situations are often even more similar than the body text, since the examples may use both (or all) of the similar methods or properties to begin with, thereby requiring no real changes when reused. So throw out the example and write a new one, or at least provide multiple examples, with at least some of them different.
- Include descriptions of each example. Both an overview of what the example does as well as coverage of how it works, in an appropriate level of detail given the complexity of the topic and the target audience, should be included.

The easiest way to avoid being overly similar is of course to write each article from scratch if time allows.

## 避免页面内容过短

如果文章过短，那么搜索引擎可能会难以甚至无法对其建立关键字索引。一般来说，文章的主体内容应该至少包含 250-300 个单词。但是也不要对内容确实很少的文章进行刻意的扩充，在可能的情况下尽量遵守该指导原则即可。

- Keep an eye on the convenient word counter located in the top-right corner of the editor's toolbar on MDN. This is not an exact representation of the true word count, since the true word count is based on the rendered page, not the page as you see it in the editor. That means macros that add a lot of words will result in a higher word count, while macros that insert nothing but adjust formatting will result in a lower word count.
- Obviously, if the article is a stub, or is missing material, add it. We try to avoid outright "stub" pages on MDN, although they do exist, but there are plenty of pages that are missing large portions of their content.
- Generally review the page to ensure that it's structured properly for the [type of page](/en-US/docs/MDN/Contribute/Structures/Page_types) it is. Be sure every section that it should have is present and has appropriate content.
- Make sure every section is complete and up-to-date, with no information missing. Are all parameters listed and explained? Make sure any exceptions are covered (this is a particularly common place where content is missing).
- Be sure everything is fully fleshed-out. It's easy to give a quick explanation of something, but make sure that all the nuances are covered. Are there special cases? Known restrictions that the reader might need to know about?
- There should be examples covering all parameters or at least the parameters (or properties, or attributes) that users from the beginner through intermediate range are likely to use, as well as any advanced ones that require extra explanation. Each example should be preceded with an overview of what the example will do, what additional knowledge might be needed to understand it, and so forth. After the example (or interspersed among pieces of the example) should be text explaining how the code works. Don't skimp on the details and the handling of errors in examples; readers _will_ copy and paste your example to use in their own projects, and your code _will_ wind up used on production sites! See [Code examples](/en-US/docs/MDN/Contribute/Structures/Code_examples) and our [Code sample guidelines](/en-US/docs/MDN/Contribute/Guidelines/Code_samples) for more useful information.
- If there are particularly common use cases for the feature being described, talk about them! Instead of assuming the reader will figure out that the method being documented can be used to solve a common development problem, actually add a section about that use case with an example and text explaining how the example works.
- Include proper {{htmlattrxref("alt", "img")}} text on all images and diagrams; this text counts, as do captions on tables and other figures.
- Do _not_ descend into adding repetitive, unhelpful material or blobs of keywords, in an attempt to improve the page's size and search ranking. This does more harm than good, both to content readability and to our search results.

## See also

- [Contributing to MDN](/en-US/docs/MDN/Contribute)
- [Writing style guide](/en-US/docs/MDN/Contribute/Guidelines/Writing_style_guide)
