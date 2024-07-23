---
title: "Tag"
date: 2022-02-01 00:01:01Z
description: "Use the tag component to show users the status of something."
---

Use the tag component to show users the status of something.

## When to use this component
Use the tag component when it’s possible for something to have more than one status and it’s useful for the user to know about that status. For example, you can use a tag to show whether an item in a task list has been ‘completed’.

## How it works
Tags are just used to indicate a status, so do not add links. Use adjectives rather than verbs for the names of your tags. Using a verb might make a user think that clicking on them will do something.

Do not use tags to create links, buttons or other interactive elements, as users:

- are unlikely to identify the tags as something they’re meant to interact with
- would see no visual difference between interactive and non-interactive tags

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<span class="govcy-tag">COMPLETED</span>
</div>

*HTML code*
```html
<span class="govcy-tag">COMPLETED</span>
```
### Showing one or two statuses
Sometimes a single status is enough. For example if you need to tell users which parts of an application they’ve finished and which they have not, you may only need a ‘Completed’ tag. Because the user understands that if something does not have a tag, that means it’s incomplete.

The [task list pattern](../../patterns/task-list-page/) has an example of how to show one status using tags.

Or it can make sense to have two statuses. For example you may find that there’s a need to have one tag for ‘Active’ users and one for ‘Inactive’ users.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<table class="govcy-table">
    <thead>
        <tr class="govcy-br-input">
            <th>Name of user</th>
            <th>Status</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Kyriacou Antonis</td>
            <td><span class="govcy-tag govcy-tag-gray">INACTIVE</span></td>
        </tr>
        <tr>
            <td>Andreou Andreas</td>
            <td><span class="govcy-tag">ACTIVE</span></td>
        </tr>
        <tr>
            <td>Mariou Daphne</td>
            <td><span class="govcy-tag">ACTIVE</span></td>
        </tr>
        <tr>
            <td>Kyprou Paraskevi</td>
            <td><span class="govcy-tag govcy-tag-gray">INACTIVE</span></td>
        </tr>
    </tbody>
</table>
</div>

*HTML code*
```html
<table class="govcy-table">
    <thead>
        <tr class="govcy-br-input">
            <th>Name of user</th>
            <th>Status</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Kyriacou Antonis</td>
            <td><span class="govcy-tag govcy-tag-gray">INACTIVE</span></td>
        </tr>
        <tr>
            <td>Andreou Andreas</td>
            <td><span class="govcy-tag">ACTIVE</span></td>
        </tr>
        <tr>
            <td>Mariou Daphne</td>
            <td><span class="govcy-tag">ACTIVE</span></td>
        </tr>
        <tr>
            <td>Kyprou Paraskevi</td>
            <td><span class="govcy-tag govcy-tag-gray">INACTIVE</span></td>
        </tr>
    </tbody>
</table>
```
### Showing multiple statuses
Tags should be helpful to users. The more you add, the harder it is for users to remember them. So start with the smallest number of statuses you think might work, then add more if your user research shows there’s a need for them.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<table class="govcy-table">
    <thead>
        <tr class="govcy-br-input">
            <th>Name of user</th>
            <th>Status</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Kyriacou Antonis</td>
            <td><span class="govcy-tag govcy-tag-orange">URGENT</span></td>
        </tr>
        <tr>
            <td>Andreou Andreas</td>
            <td><span class="govcy-tag govcy-tag-blue">NEW</span></td>
        </tr>
        <tr>
            <td>Mariou Daphne</td>
            <td><span class="govcy-tag govcy-tag-green">FINISHED</span></td>
        </tr>
        <tr>
            <td>Kyprou Paraskevi</td>
            <td><span class="govcy-tag govcy-tag-yellow">WAITING ON</span></td>
        </tr>
    </tbody>
</table>
</div>

*HTML code*
```html
<table class="govcy-table">
    <thead>
        <tr class="govcy-br-input">
            <th>Name of user</th>
            <th>Status</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Kyriacou Antonis</td>
            <td><span class="govcy-tag govcy-tag-orange">URGENT</span></td>
        </tr>
        <tr>
            <td>Andreou Andreas</td>
            <td><span class="govcy-tag govcy-tag-blue">NEW</span></td>
        </tr>
        <tr>
            <td>Mariou Daphne</td>
            <td><span class="govcy-tag govcy-tag-green">FINISHED</span></td>
        </tr>
        <tr>
            <td>Kyprou Paraskevi</td>
            <td><span class="govcy-tag govcy-tag-yellow">WAITING ON</span></td>
        </tr>
    </tbody>
</table>
```
### Using colour with tags
If you are using tags to show progress, use the [text and colours of the task list](../../patterns/task-list-page/#status-text-and-style). 

You can use colour to help distinguish between different tags – or to help draw the user’s attention to a tag if it’s especially important. For example, it probably makes sense to use `govcy-tag-orange` for a tag that reads ‘Urgent’.

If you need more tag colours, you can use the following classes.

*Example*
<div class="govcy-container govcy-p-4 govcy-br-1 govcy-br-standard govcy-mb-4">
<table class="govcy-table">
    <thead>
        <tr class="govcy-br-input">
            <th>Class name</th>
            <th>Tag</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>govcy-tag</td>
            <td><span class="govcy-tag">INACTIVE</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-gray</td>
            <td><span class="govcy-tag govcy-tag-gray">COMPLETED</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-darkgreen</td>
            <td><span class="govcy-tag govcy-tag-darkgreen">PENDING</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-green</td>
            <td><span class="govcy-tag govcy-tag-green">FINISHED</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-purple</td>
            <td><span class="govcy-tag govcy-tag-purple">SENT</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-blue</td>
            <td><span class="govcy-tag govcy-tag-blue">NEW</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-red</td>
            <td><span class="govcy-tag govcy-tag-red">DECLINED</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-orange</td>
            <td><span class="govcy-tag govcy-tag-orange">URGENT</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-yellow</td>
            <td><span class="govcy-tag govcy-tag-yellow">DELAYED</span></td>
        </tr>
    </tbody>
</table>
</div>

*HTML code*
```html
<table class="govcy-table">
    <thead>
        <tr class="govcy-br-input">
            <th>Class name</th>
            <th>Tag</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>govcy-tag</td>
            <td><span class="govcy-tag">INACTIVE</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-gray</td>
            <td><span class="govcy-tag govcy-tag-gray">COMPLETED</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-darkgreen</td>
            <td><span class="govcy-tag govcy-tag-darkgreen">PENDING</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-green</td>
            <td><span class="govcy-tag govcy-tag-green">FINISHED</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-purple</td>
            <td><span class="govcy-tag govcy-tag-purple">SENT</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-blue</td>
            <td><span class="govcy-tag govcy-tag-blue">NEW</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-red</td>
            <td><span class="govcy-tag govcy-tag-red">DECLINED</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-orange</td>
            <td><span class="govcy-tag govcy-tag-orange">URGENT</span></td>
        </tr>
        <tr>
            <td>govcy-tag govcy-tag-yellow</td>
            <td><span class="govcy-tag govcy-tag-yellow">DELAYED</span></td>
        </tr>
    </tbody>
</table>
```

## Accessibility
[Do not use colour alone to convey information (opens in new tab)](https://www.w3.org/WAI/WCAG21/Understanding/use-of-color.html){rel="noreferrer noopener" target="_blank"} because it’s not accessible. If you use the same tag in more than one place, make sure you keep the colour consistent.