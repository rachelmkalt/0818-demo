---
title: Intro to Bi-Directional Sync
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

Our bi-directional sync feature allows you to effortlessly connect your documentation in ReadMe with your Git repositories, empowering your team to work where they thrive. Whether you prefer the intuitive ReadMe editor or your favorite Git workflow, this powerful integration ensures that your documentation is always up-to-date and easily accessible.

For a step-by-step walkthrough of getting started with Bi-Directional Sync, we recommend watching this tutorial:

<Embed url="https://www.youtube.com/watch?v=D_GAl5oYzTA" title="ReadMe Refactored: New Editing UI and Bi-Directional Sync with GitHub" favicon="https://www.youtube.com/favicon.ico" image="https://i.ytimg.com/vi/D_GAl5oYzTA/hqdefault.jpg" provider="youtube.com" href="https://www.youtube.com/watch?v=D_GAl5oYzTA" typeOfEmbed="youtube" html="%3Ciframe%20class%3D%22embedly-embed%22%20src%3D%22%2F%2Fcdn.embedly.com%2Fwidgets%2Fmedia.html%3Fsrc%3Dhttps%253A%252F%252Fwww.youtube.com%252Fembed%252FD_GAl5oYzTA%253Ffeature%253Doembed%26display_name%3DYouTube%26url%3Dhttps%253A%252F%252Fwww.youtube.com%252Fwatch%253Fv%253DD_GAl5oYzTA%26image%3Dhttps%253A%252F%252Fi.ytimg.com%252Fvi%252FD_GAl5oYzTA%252Fhqdefault.jpg%26type%3Dtext%252Fhtml%26schema%3Dyoutube%22%20width%3D%22854%22%20height%3D%22480%22%20scrolling%3D%22no%22%20title%3D%22YouTube%20embed%22%20frameborder%3D%220%22%20allow%3D%22autoplay%3B%20fullscreen%3B%20encrypted-media%3B%20picture-in-picture%3B%22%20allowfullscreen%3D%22true%22%3E%3C%2Fiframe%3E" />

<br />

## What is Bi-Directional Sync?

Bi-directional sync creates a two-way connection between your ReadMe project and a Git repository. When you make changes in either location:

* Changes made in ReadMe are automatically synced to your Git repository.
* Changes pushed to your Git repository are automatically reflected in ReadMe.
* Content stays consistent across both platforms without manual copying or updating.

## Key Benefits

* **Write Where You Want**: Give your team the flexibility to work in their preferred environment - whether that's ReadMe's editor UI or their local development setup.
* **Version Control**: Leverage Git's powerful version control capabilities for your documentation.
* **Automated Syncing**: Changes sync automatically between platforms, eliminating manual updates.
* **Collaboration**: Enable developers, engineers, and technical writers to collaborate seamlessly using familiar tools
* **Single Source of Truth**: Maintain consistency by having documentation synced across platforms.

## How It Works

1. **Connection Setup**: Install the **ReadMe Sync** GitHub App in your repository to establish the connection.
2. **File Structure**: Documentation is organized in a standardized folder structure:
   ```
   📂 project
   ├── 📁 guides
   ├── 📁 recipes 
   ├── 📁 custompages
   ├── 📁 references
   └── 📃 sidebar.yml
   ```
3. **Content Format**:
   * Documentation pages are stored as Markdown files with frontmatter metadata.
   * Navigation and page order are managed through `sidebar.yml` files.
   * Content supports both standard Markdown and ReadMe's enhanced features.

## Git Integration Details

ReadMe integrates through [GitHub Apps](https://docs.github.com/en/apps/overview) to provide:

* Easy installation process
* Transparent permission management
* Granular repository access controls
* Ability to modify or revoke access at any time

### Required Permissions

Repository-level access:

* **Metadata** (Read-only): Required for basic GitHub functionality
* **Contents** (Read & write): Used to sync documentation content

The integration uses webhooks to:

* Detect changes in either platform
* Trigger sync operations
* Maintain content consistency
* Handle conflict resolution

## Versioning Support

Documentation versions are handled through Git branches:

* Default branch represents your main documentation version
* Additional branches can be created for other versions
* Version metadata (public/deprecated status) is managed in ReadMe

## Getting Started

> 🚧 Empty Git repository required
>
> To successfully connect your ReadMe project, your new Git repository must be **completely empty** — including no commit history and no files such as a README.md. After you've connected, removing and adding files will work as usual.

To begin using bi-directional sync:

1. Create a new Git repository for your documentation.
2. Install the **ReadMe Sync** GitHub App.
3. Connect your ReadMe project to the repository.
4. Start writing documentation in either platform.

For more detailed information about working with bi-directional sync, see our "Editing with Bi-Directional Sync" guide.

## Enterprise Server

If you use your own hosted GitHub Enterprise Server (GHES), you can set-up syncing from your Group dashboard under Git Connection. If this option isn’t available for your project, please contact your Customer Success Manager. Keep in mind we require internet access to sync to your GHES server and syncing will not work if your server is behind a VPN.

1. To begin using bi-directional sync:
2. Create a new GitHub app for your organization.
3. Grant ReadMe access to your new, empty repository in your organization.
4. Connect a new repository to your child project.
