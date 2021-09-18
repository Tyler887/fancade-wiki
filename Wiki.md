---
title: Fancade Wiki
---

*The wiki is developed by [[Nikita Ivanov (ViChyavIn)|ViChyavIn]], Olle Landin, and [[Martin Magni]].*

This wiki helps users learn more about Fancade and one of its [[game-making tools|Build]]. Pages are written by Fancaders themselves. Maybe you want to help improve the wiki too?

[[_TOC_]]

# Rules

Yes? You'd like to contribute? Great!! Here's some advice to help you get started editing.

## Write about Fancade

The wiki is about [Fancade](https://fancade.com), so try to stay on topic.

## Create your page

Before creating a brand *new* wiki page, check if:

* The page already exists, just with a slightly different name?
* The info doesn't fit better as a note on an existing page?
* The page is likely to be useful to other Fancade users?

## Don't save unfinished edits

Don't leave articles in WIP state.

If you're not done yet, but you can't continue working right now, you can always quit the editor and keep editing next time. The wiki will remember the state of the page you were editing and will prompt you to recover it when you enter the editor!

## Don't ask readers to answer unanswered questions

If you're not sure about something, don't ask future editors to correct you in the page, for example:

<blockquote>
[[Constraints]] are very hard to learn. Maybe it is just me?
</blockquote>

Those who can answer your question will rarely visit the page, so you will end up throwing your question at readers'. Feel free to join our Fancade [[Discord]] and ask your question there, in order to provide the most accurate information to our readers!

# How-to

Want to help but have no idea how it's done? Okay! Read below to learn how to format text and create new pages...

## Create a page

In the Wiki page, there is an ability to create new pages, simply by clicking "New". A pop-up with the title "Create New Page" should show up.

Create a page name with the appropriate title.

If you are writing it in a different folder (e.g. Build) write `<folder>/<title>` (e.g. `Build/Set Variable`) to create it within this section.

Now you can write a Wiki page! After you have written it all, click "Preview" to make sure everything looks correct.

## Style a page

Fancade Wiki uses the formatting syntax called "Markdown". You can make text **bold**, *italic*, ***bolditalic***, and ~~strikethrough~~. Not just that, you can also make a list, add links, insert images and even make tables! To learn more, read [[this|https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet]].

### Basics

#### Add link

To insert a link, you can:

| Wrap page name in square brackets | `[[Number]]` | [[Number]]
| Wrap page name in square brackets and put a suffix | `[[Number]]s` | [[Number]]s
| Wrap page name in square brackets and set displayed text | `[[One|Number]]` | [[One|Number]]
| Wrap URL in square brackets | `[[http://fancade.com/]]` | [[http://fancade.com/]]
| Wrap URL in square brackets and set displayed text | `[[Fancade|http://fancade.com/]]` | [[Fancade|http://fancade.com/]]

#### Make list

To insert a list element, put `*`, `+` or `-` at the beginning of a line. For example:

```
* Fancade
* is the fanmade
* arcade
```
will be

* Fancade
* is the fanmade
* arcade

#### Add image

To add an image, drag-n-drop it into the edit form. (It will be uploaded to `/uploads/<filename>`)

To insert an existing image, you wrap the image path/URL in square brackets like you do with regular links/URLs to insert it directly in the text.

`[[uploads/image.jpg]]`

You can also upload an image by clicking "Upload" button in edit mode.

(The only area a image can be uploaded by default is /uploads.)

#### Add heading

Use hashes then a space at the start of your text. Here is a example:

```
## Fancade
## is the fanmade
## arcade
```

#### Code font

To use a coding text font, use a grave accent at the start and end of your text without any spaces between both of the grave accents. For example:

Fancade > `Fancade`

If you want newlines, then you need 3 grave accents before the first line and another three after the last line. (This lets you show colors based on code languages using Coffeescript, just put `coffeescript` on the line that comes after the first three grave accents.) For example:

Before:

Fancade

is the fanmade

arcade

After:
```
Fancade
is the fanmade
arcade
```

## Delete a page

Deleting a page is possible, but restricted:

* If you are not a Fanmod: Ping a Fanmod on our Fancade [[Discord]] and suggest the deletion to them.
* If you are a Fanmod: Use extra wiki page delete commands in Fanbot.

## Revert a change

Go to the latest changes in the update history of a page, check the commit, compare it and revert it.

## Rename a page

Click Rename and enter the new page name.

## Sign out

There's no button to sign out. But if you clear the website data in your browser settings, you will be signed out. (It is a cookie??)

## Notes

* On keyboards, you can switch between edit and preview modes with `CTRL+Shift+P`.
