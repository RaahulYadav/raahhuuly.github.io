---
title: "Markdown and Math Tutorial"
date: 2026-05-15
permalink: /posts/2026/05/markdown-tutorial/
tags:
  - Tutorial
  - Markdown
  - LaTeX
---

# Welcome to your Markdown Tutorial!

Since you are familiar with LaTeX and Overleaf, Markdown will feel like a "lite" version of what you already know. Here is how to do the things you asked for.

## 1. Text Emphasis
- **Bold**: Use `**text**` to get **bold text**.
- *Italic*: Use `*text*` to get *italic text*.
- ***Bold and Italic***: Use `***text***`.

## 2. Mathematics (LaTeX Style)
Your website uses MathJax, so you can write LaTeX equations directly.

- **Inline Math**: Use double dollar signs around small expressions: $$E=mc^2$$. 
  *Note: In this specific theme, it seems single dollar signs are also often used for inline math.*
- **Display Math**: Use double dollar signs on their own lines for centered equations:
  
  $$
  \mathcal{L} = \frac{1}{2} \partial_\mu \phi \partial^\mu \phi - \frac{1}{2} m^2 \phi^2
  $$

## 3. Links
- **External Links**: `[Text](URL)`
  Example: [My GitHub Profile](https://github.com/raahhuuly)
- **Internal Links**: 
  - To link to your "About" page: `[About Me](/about/)`
  - To link to another post: Use the permalink defined in that post's header. 
    Example: [Read about the constant e](/posts/2026/04/what-is-e/)

## 4. Lists
- Use `-` or `*` for bullet points.
- Use `1.` for numbered lists.

## 5. Code Blocks
If you want to show code, wrap it in triple backticks:

```python
def hello_world():
    print("Hello from Markdown!")
```

## 6. Images
To include an image, use this syntax: `![Alt Text](/images/filename.jpg)`

- **Alt Text**: This is what screen readers see and what shows up if the image fails to load.
- **Path**: Always start with `/images/` if that is where you saved your file.

Example using an image already in your repository:
![My Profile Photo](/images/profile.png)

> [!TIP]
> If you want to center an image or resize it, you can use standard HTML inside your Markdown:
> `<img src="/images/profile.png" width="200" style="display: block; margin: 0 auto;">`

## How it works
When you save this file in the `_posts` folder, the Jekyll engine (running in your Docker container) sees the new file, converts the Markdown syntax into HTML tags, and inserts it into your website layout. 

You can see the results immediately by checking your local website URL (usually `http://localhost:4000`).
