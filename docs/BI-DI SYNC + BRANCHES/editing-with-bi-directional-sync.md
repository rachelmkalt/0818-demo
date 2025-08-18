---
title: Editing with Bi-Directional Sync
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
> 🚧 Beta
>
> Bi-directional sync is currently in beta. If you’d like to try it out, please join the waitlist in the admin dashboard, or reach out to [beta@readme.io](mailto:beta@readme.io).

# Overview

Ready to start editing with bi-directional sync? Whether you're making quick updates in ReadMe's intuitive editor or pushing changes through Git, bi-directional sync keeps everything in perfect harmony. Your edits in ReadMe automatically flow to your GitHub repository, and any changes you commit to GitHub appear right in your ReadMe hub. Don't worry about version conflicts or maintaining multiple copies – bi-directional sync handles the heavy lifting, so you can focus on creating great documentation wherever you prefer to work.

I'm editing this live!

## Setting Up Bi-Directional Sync

### Prerequisites

1. Your project must be enabled for the new editing UI.
2. You must have a GitHub account and an **empty private repository**.

<Callout icon="❕" theme="default">
  ### **Important**: Repositories must be empty on initial sync.
</Callout>

### Initial Configuration

1. Go to **Settings > Git Connection** in your ReadMe project settings.
2. Create a new empty private repository in your GitHub account.
3. Click **Sync with GitHub** in ReadMe.
4. Authenticate with GitHub when prompted.
5. Select the repositories you want ReadMe to access (including your new repo).
6. Choose your project and click **Sync Repository**.

<Image alt="This project already has a Connected Repository and is what your page will look like once your connect your ReadMe project to an empty GitHub repository!" align="center" src="https://files.readme.io/6321a9dd26b8ae4e0a317c4449ddd586a9cffdd6573e17da387265919de7b20a-CleanShot_2025-06-09_at_18.29.512x.png">
  This project already has a Connected Repository and is what your page will look like once your connect your ReadMe project to an empty GitHub repository!
</Image>

### Changing Connected Repositories

<Callout icon="❕" theme="default">
  ### **Important**: When changing repositories, you must disconnect the original repository from GitHub before proceeding.
</Callout>

If you need to connect your ReadMe project to a different GitHub repository:

1. **Disconnect the original repository**:
   * Go to your GitHub account settings
   * Navigate to "Applications" > "Installed GitHub Apps"
   * Find "ReadMe Sync" and click "Configure"
   * Either:
     * Remove access completely by clicking "Uninstall", or
     * Select "Only select repositories" and uncheck the repository you want to disconnect
2. **Connect to new repository in ReadMe**:
   * Go to **Settings > Git Connection** in your ReadMe project settings
   * Click **Sync with GitHub**
   * Follow the authentication process
   * Select your new empty repository
   * Choose your project and click **Sync Repository**

## Documentation Structure

### Project structure

Each ReadMe project will be equivalent to a GitHub repository. See the diagram below:

<Image align="center" src="https://files.readme.io/2297d27720ff8135204589d04a950f50beb805d37ea610683bcb0295056e6c11-edit_bidi_1.png" />

### File Organization

The bi-directional sync feature offers a format that closely mirrors the well-organized ReadMe project structure. With folders neatly organizing your documentation and markdown files serving as individual pages, it creates a user-friendly experience that will feel instantly familiar to ReadMe users.

Your documentation follows this standardized structure:

```
📂 project
├── 📁 guides
│   ├── 📂 category-folder
│   │   ├── 📄 page.md
│   │   └── 📃 sidebar.yml
│   └── 📃 sidebar.yml
├── 📁 recipes
├── 📁 custompages
└── 📁 references
```

Each component serves a specific purpose:

* `guides`: Contains your main documentation content, organized in categories.
* `recipes`: Holds step-by-step tutorials and how-to guides.
* `custompages`: Stores any custom pages you've created.
* `references`: Contains API reference documentation.
* `sidebar.yml`: Manages the navigation structure for each section.

This organization mirrors your ReadMe project structure, making it easy to maintain consistency between your Git repository and ReadMe documentation.

### File Format

Documentation pages use Markdown with front matter metadata:

```markdown
---
title: List all owls
api:
  file: hoot.json
  operationId: get_owls
hidden: false
metadata:
  title: My SEO Title
  description: A brief description for SEO
  keywords:
    - keyword1
    - keyword2
---

# Main Content

Your documentation content goes here...
```

### Guides Structure

Page order and navigation are controlled by `_order.yml` files:

```yaml
- welcome-page
- getting-started
- advanced-topics
  - feature-one
  - feature-two
```

### API Reference Navigation Structure

**Code Example**

```yaml
- reference:
  - Owl Sanctuary API:
    - owls:
      - postowls
      - index
      - getsightings
      - getowlsid
      - getowls
    - habitats:
      - index
      - gethabitats
```

**Image Example**

<Image align="center" width="200px" src="https://files.readme.io/64b12aa1c877732dcb40db450a91e5d95d76dad8294b8d645aa0ccfd128bab2c-edit_bidi_2.png" />

This is after uploading a sample OAS file, hoot.json. The above matches the following sidebar:

<Image align="center" width="49% " src="https://files.readme.io/b4c9830f4199906ca22ce2ff5279bc26e194239f0d18fdbdc6ed2f6be9912087-edit_bidi_3.png" />

***

## Editing in ReadMe

### Making Changes

1. Navigate to the page you want to edit in ReadMe.
2. Make your changes using the ReadMe editor.
3. Save your changes.
4. Changes will automatically sync to your Git repository.

### Handling Conflicts

When conflicts occur during saving:

1. ReadMe will display a conflict notification.
2. You can choose to:
   * Overwrite the changes in Git.
   * Cancel the save and incorporate Git changes first.
3. Review the changes carefully before deciding.

## Editing in Git

When editing documentation in Git, you can use your preferred code editor or Git tools. The bi-directional sync feature will detect changes made to your Git repository and automatically update your ReadMe documentation.

### Content Structure

1. **Markdown Files**:
   * Files must include required frontmatter (title, summary)
   * Content follows standard Markdown format.
   * File names should match the intended URL slug.

2. **Navigation**:
   * Page order is controlled by `sidebar.yml` files.
   * Each category folder can have its own `sidebar.yml`
   * Navigation structure mirrors your ReadMe project.

## Managing Versions

### Version Control with Git

* Each documentation version corresponds to a Git branch.
* The default branch represents your main version
* Create new branches for major versions:
  ```shell
  git checkout -b v2.0
  ```

### Version Settings

Version-specific settings like public/deprecated status are managed in ReadMe's interface, not in Git.

## Conflict Resolution

### Handling Conflicts in ReadMe

When a conflict is detected while saving in ReadMe, the system will:

1. Display a conflict notification indicating changes were made in another session
2. Present you with two options:
   * Overwrite the changes in Git
   * Cancel the save and continue editing

This gives you the chance to check for changes made in Git and incorporate those changes manually in the ReadMe editor before saving again.

### Handling Conflicts Outside ReadMe

Users who run into conflicts will be able to resolve those conflicts using their preferred tool:

* Manually in a code editor
* Tools offered by their Git service
* Other preferred conflict resolution methods

## Branch Synchronization

When working with branches across ReadMe and GitHub, there are some important synchronization behaviors to understand:

### Creating Branches in ReadMe

* The initial commit in ReadMe is required to establish the branch synchronization with GitHub.

### Creating Branches in GitHub

* If you create a branch in GitHub, you must create a corresponding version in ReadMe with the same name.
* While the branch exists in GitHub, ReadMe won't recognize it until you create the matching version in the ReadMe interface.

### Synchronizing Branch Content

* After the initial ReadMe change, all content from both GitHub and ReadMe will be synchronized (assuming there aren't any conflicts).

## Working with GitHub Branch Protection

If your GitHub repository uses branch protection rules, you'll need to configure them to allow the ReadMe Sync app to push changes. Here's how to set it up based on your GitHub configuration:

### For GitHub Rulesets (New Version)

1. Navigate to your repository's branch protection settings.
2. Look for the **Bypass list** section.
3. Click **+ Add bypass**.
4. Search for "ReadMe Sync" (App • readmeio).
5. Set the permission to **Always allow**.

<Image align="center" src="https://files.readme.io/38320eee1583302ae1104f563d0d9e689cd7290358807e60c164dcc28e507717-edit_bidi_4.png" />

### For Legacy Branch Protection

1. Go to your repository's branch protection rules.
2. Find the **Allow specified actors to bypass required pull requests** section.
3. Click the search box.
4. Add "readme-sync" (ReadMe Sync) to the allowed actors list.

<Image align="center" src="https://files.readme.io/4020ddf36bc045d444a47115fea15486a2d559c1fd0d90d7f3658605a904cc65-edit_bidi_5.png" />

This configuration ensures that changes made in ReadMe's editor can be synchronized to protected branches in your GitHub repository.
