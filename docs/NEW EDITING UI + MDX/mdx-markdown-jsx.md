---
title: MDX (Markdown + JSX)
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

As part of the upgrade to ReadMe Refactored, we also migrated ReadMe's entire editor from Markdown to MDX. MDX combines the simplicity of Markdown with JSX, providing content creators and developers alike with a familiar syntax to create dynamic and interactive documentation. Now, teams in ReadMe can build their own reusable MDX components using a combination of React, JSX, and Tailwind styling and add them to the Custom Components page in the Editing UI of a child project, or at the Group level, in the Custom Components page of your Enterprise Group. We also pre-built five MDX components—cards, accordion, tabs, columns, and mermaid.js diagrams—which are available via the editor slash menu in your Editing UI.

Here's an example of a component built using MDX:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/53e6b26f9e793c6940faf66a830c1af2f592620934954de384e4eec3000c157d-stepper_preview_for_blog_post.gif",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


## What is MDX?

[MDX](https://mdxjs.com/), which blends Markdown and embedded JSX, is built on top of React. If you’ve ever written Markdown, which you've surely done if you've written content in ReadMe, you know how easy it is to format text with simple symbols—like using # for headings or **bold** for emphasis. MDX takes that simplicity and combines it with the power of [React components](https://react.dev/), allowing your team to write interactive and dynamic content right inside Markdown files.

You can think of MDX as a supercharged ⚡️ version of Markdown. It lets you mix plain text with React components to build interactive UI elements—like buttons, graphs, terminal windows, or even responsive tables—and the React components give the components their dynamic behavior.

ReadMe’s Custom Components feature also has built-in Tailwind CSS styling support. [Tailwind](https://tailwindcss.com/) is a utility-first framework that helps us style elements quickly so that rather than writing long CSS files, you can instead add class names directly inside our components.

MDX extends traditional Markdown by enabling you to:

- Import and use React components in your documentation
- Create interactive documentation elements
- Build reusable custom components
- Enhance your docs with dynamic features

## Why Use MDX?

### Enhanced Creativity

- Add interactive components to explain complex concepts
- Create custom behaviors for your documentation
- Build dynamic examples and demonstrations

### Improved Reusability

- Write components once, use them throughout your docs
- Maintain consistency across your documentation
- Update shared components in one place

### Future-Proof Documentation

- Scale your documentation with your product
- Add new interactive features as needed
- Maintain modern, dynamic documentation