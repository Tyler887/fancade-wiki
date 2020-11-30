The Wiki supports the same formatting syntax as Discord, which is called "[[Markdown|https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet]]". So you can easily make *italic*, **bold**, __underlined__ or ~~strikethrough~~ text. To learn how, read [[this|https://support.discordapp.com/hc/en-us/articles/210298617-Markdown-Text-101-Chat-Formatting-Bold-Italic-Underline-]].

Besides, there are such Wiki-exclusive formatting features as unordered lists, links and images in text.

To insert a list element, put `*`, `+` or `-` at the beginning of a line. Note that there must be one blank line before the first element.

To insert a link, you can:

* wrap page name in square brackets: [[Add]] `[[Add]]`
* do the same but put a suffix if needed: [[Vector]]s `[[Vector]]s`
* wrap page name in parentheses and set displayed text in square brackets before: [[Plus|Add]] `[[Plus|Add]]`
* do the same but put any URL instead of a page name: [[Fancade|http://fancade.com/]] `[[Fancade|http://www.fancade.com/]] `

To insert an image, you can:

* Attach an image or a video to a message you're about to tag. The media will appear in the bottom of a page. The same works if you use `.tag edit` command (but keep in mind it'll overwrite old attachments)
* Use `.tag attachment add` command
* Wrap image URL in `!` to insert it directly in the text
* Add additional exclamation mark before the first one if you don't want the image to appear when calling `.wiki`