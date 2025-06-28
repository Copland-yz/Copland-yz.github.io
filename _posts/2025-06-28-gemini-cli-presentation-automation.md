---
title: "Automating Presentation Creation from Research Papers with Gemini-CLI"
date: 2025-06-28
tags: [Gemini, CLI, Automation, Research, Workflow]
---

Creating presentations from dense research papers can be a time-consuming process. You have to read the paper, extract the key points, find the relevant figures, and then assemble everything into a coherent slideshow. But what if this entire workflow could be automated?

With the Gemini-CLI, this is now a reality.

I've been exploring how to use the command-line interface of Gemini to build a fully automated pipeline that takes a journal paper's URL as input and outputs a presentation file (like a PowerPoint .pptx).

The key is that Gemini-CLI can not only understand the content of the paper but also execute shell commands. This is a game-changer. It means the AI can:

1.  **Fetch and Read the Paper:** Given a URL to a PDF of a research paper, Gemini can access and process its content.
2.  **Summarize Key Points:** It can intelligently summarize the abstract, introduction, methods, results, and conclusion, creating a narrative for the presentation.
3.  **Extract Figures:** This is the most powerful part. Gemini-CLI can be instructed to use command-line tools (like `wget` or `curl`) to download the images and figures directly from the paper's source if they are accessible. It can identify the figures in the paper and then use the URL to download them locally.
4.  **Generate Presentation Content:** Finally, it can structure the summarized text and the paths to the downloaded images into a format that can be programmatically converted into a presentation. For example, it could generate Markdown that can then be converted to a `.pptx` file using a tool like `pandoc`.

This creates a seamless, "zero-touch" workflow. You provide a URL, and you get a presentation.

Here is a glimpse of the workflow in action:

![Gemini-CLI identifying figures in a paper](/images/gemini-workflow-example1.jpg)

And here is the command-line tool being used to download an image:

![Gemini-CLI using a shell command to download a figure](/images/gemini-workflow-example2.jpg)

The potential for this to streamline how researchers and students communicate their findings is enormous.
