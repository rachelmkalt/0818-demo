---
title: Intro to Branches
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
> This feature is in active development and may change before final release. Feedback is always appreciated at [beta@readme.com](beta@readme.com).

Branches allow ReadMe Admins to save changes across pages without them going live immediately. With branches, you can continue to edit as you always have! Branches are an optional workflow that offer flexibility in your writing process. Writers use branches to:

* Make changes and review them in a preview environment before they’re live.
* Send changes to teammates for review.
* Make changes across multiple pages.

<Callout icon="💁‍♂️" theme="default">
  ### **Note:** Additional review options are only available on Enterprise plans.
</Callout>

***

## Creating a Branch

There are three ways to create a branch:

1. Navigate to the versions and branches menu. Once there, you can create new branches from a version.
2. While editing a version, instead of saving you can save to a new branch.
3. If you’re [syncing with GitHub](https://docs.readme.com/main/docs/bi-directional-sync) , branches created in GitHub will show up in ReadMe. And branches created in the ReadMe UI will automatically show up in GitHub!

Once your branch is created, you can start writing! Changes will not be live until you merge your branch into a public version.

<Image align="center" src="https://files.readme.io/66750bb4ffdf062a43e77e2ce1a3bfc6d36a2c6fa670e3968b621159ab7b177a-branches_1.png" />

There are no time limit or expiration on branches. Any admin on your team can view, edit, merge, and delete any branch.

## Merging a Branch

Once you’re ready for the changes to go live, you can merge from the branch menu:

<Image align="center" src="https://files.readme.io/51f1614616e3ee1fac70268bd784076acd002ec15809843ee495b576f0a31086-branches_2.png" />

On merge, a check will be run to ensure there are no merge conflicts. If there are conflicts that must be resolved, we recommend [resolving the conflicts from GitHub](https://docs.readme.com/main/docs/branches#/handling-conflicts). If your project does not sync with GitHub, you can to ignore the conflict and forcefully merge their changes—with preference to the changes in the branch.

Once merged, your branches are not deleted so you can review the changes before deleting them.

<Callout icon="💁‍♂️" theme="default">
  ### GitHub users can merge a branch into a version too—including via Pull Requests.
</Callout>

***

## Syncing with GitHub

You do not have to sync with GitHub to use branches.

When creating branches from GitHub, their name has to be formatted to include their version: `{version}_{branch}`. Examples:

```
v2.0_rewrite-getting-started
v2.0_add-new-feature
v2.0_fix-typo
```

### Access & Permissions

ReadMe and GitHub permissions are independent. Users with access to your GitHub project’s branches will have access to any content changes. In order for users to view content changes made in branches via GitHub, they will need a ReadMe account with access to your project’s branch.

### Handling Conflicts

When merging from GitHub, the user can resolve conflicts via the GitHub editor or the merge tool of their choice locally before pushing.

When merging from ReadMe, the changes you see when previewing will always match what goes lives when merging. Conflicting changes from GitHub will not appear.

***

## FAQ

<Accordion title="Who can view a branch?" icon="fa-help-circle">
  At this time, anyone with the link can view a branch.
</Accordion>
