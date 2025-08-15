---
title: ReadMe Refactored Snapshot
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
# Overview

We're excited to introduce our new editing experience that brings powerful features including bi-directional Git syncing, branching, MDX support, and a streamlined editing interface. **This page provides a high level overview on everything that's new.**

## What's New

We've refactored every part of ReadMe to support the next generation of APIs, making it easier for people with all levels of technical skills to contribute! Check out the new features and don't miss the full feature list further down—we're just getting started.

<Cards columns={4}>
  <Card title="ReadMe's New UI" icon="fa-duotone fa-book-open-cover" target="_blank">
    Create and edit your docs with a new design that brings your content and appearance changes closer to what your users see.
  </Card>

  <Card title="MDX Support" icon="fa-duotone fa-code">
    Enhance your docs with interactive components by combining the simplicity of Markdown with the power of JSX.
  </Card>

  <Card title="Bi-Directional Git Sync" icon="fa-duotone fa-sync">
    Write documentation wherever works best for you, seamlessly syncing between ReadMe and your Git repositories.
  </Card>

  <Card title="Branching" icon="fa-duotone fa-solid fa-code-branch">
    Expand your workflow in ReadMe! With Branching, Admins can make changes and review them in a preview environment before they’re live.
  </Card>
</Cards>

### See It In Action

Watch the video to get a firsthand look at how the new features work and feel!

<Embed url="https://www.youtube.com/watch?v=Wwly83u-ALY" title="Getting Started with ReadMe Refactored" favicon="https://www.youtube.com/favicon.ico" image="https://i.ytimg.com/vi/Wwly83u-ALY/hqdefault.jpg" provider="youtube.com" href="https://www.youtube.com/watch?v=Wwly83u-ALY" typeOfEmbed="youtube" html="%3Ciframe%20class%3D%22embedly-embed%22%20src%3D%22%2F%2Fcdn.embedly.com%2Fwidgets%2Fmedia.html%3Fsrc%3Dhttps%253A%252F%252Fwww.youtube.com%252Fembed%252FWwly83u-ALY%253Ffeature%253Doembed%26display_name%3DYouTube%26url%3Dhttps%253A%252F%252Fwww.youtube.com%252Fwatch%253Fv%253DWwly83u-ALY%26image%3Dhttps%253A%252F%252Fi.ytimg.com%252Fvi%252FWwly83u-ALY%252Fhqdefault.jpg%26type%3Dtext%252Fhtml%26schema%3Dyoutube%22%20width%3D%22640%22%20height%3D%22480%22%20scrolling%3D%22no%22%20title%3D%22YouTube%20embed%22%20frameborder%3D%220%22%20allow%3D%22autoplay%3B%20fullscreen%3B%20encrypted-media%3B%20picture-in-picture%3B%22%20allowfullscreen%3D%22true%22%3E%3C%2Fiframe%3E" />

<Callout icon="📌" theme="default">
  ### Feature Compatibility

  We're continuing to release new features for Refactored as we work toward full feature parity, and keep our docs updated to notify you of all new updates and improvements. If a feature that you use isn't currently available on the Refactored experience, rest assured that it'll be available soon!

  For the most recent list, refer to this breakdown in our docs: [https://docs.readme.com/main/docs/migration#/feature-compatibility](https://docs.readme.com/main/docs/migration#/feature-compatibility)
</Callout>

## Enterprise Users

> 🚧 Important Note for Enterprise Customers
>
> The new ReadMe experience has begun rolling out to Enterprise customers! If you have access to playground project like this, it means your Enterprise Group is ready—or very close—to migrating. 🎉
>
> The ReadMe team is here to help you manage every step of the upgrade process, including the migration process itself. Now that you have access to this playground environment, your CSM will be in touch to discuss next steps, including setting a migration date for your team.

### New and Improved Enterprise Features

You'll have access to all standard features mentioned above plus:

* Global Custom Components, in addition to Custom Components in your child projects
* Advanced branching features including review and approval processes—an upgrade to Staging! (Coming soon)
* Bi-Directional Syncing compatibility with your Enterprise team's own hosted GitHub Enterprise Server (GHES), if applicable
* Enhanced team collaboration tools
* Comprehensive audit logging
* Enterprise-grade security features

### What's Missing

If you're currently using any features listed below, your Enterprise Group is not quite ready to migrate. While we're working to build these feature, your CSM can explain what the timeline looks like, and potential workarounds.

* AWS Gateway Plugin
* Suggested Edits - branches replaces the previous Suggested Edits internal workflow of allowing team members to leave edits and comments; we are working to build a solution in Refactored that allows visitors to propose changes!
