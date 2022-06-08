---
title: "VIM tip: How to quickly increment or decrement a number within VIM"
date: 2022-06-08
showToc: false
TocOpen: false
hidemeta: false
comments: false
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowRssButtonInSectionTermList: true
draft: false
tags: [VIM, Tip]
---

# Introduction

I recently came upon a very interesting trick to quickly increment or decrement a number within VIM. These simple shortcut keys are really helpful in case we made a small mistake and don't want to rewrite the whole number.

# Example

Let's assume we have the following text in our current file: 

```
Good morning Sir, I would like to buy 4 peaches.
```

With the cursor at the beginning of the line, we can press _\<Ctrl-a\>_ to increase or _\<Ctrl-x\>_ to decrease the `4` in the above text. It is important to note that this will increase/decrease the number under the cursor or the next available number in the text. It might therefore be necessary to jump to the desired number before using the above shortcut.

We can furthermore specify the value to add or subtract by defining it before executing the shortcut. For example, pressing _10\<Ctrl-a\>_ will change the text to:

```
Good morning Sir, I would like to buy 14 peaches.
```
