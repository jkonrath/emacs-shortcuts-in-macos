# emacs-shortcuts-in-macos
A tutorial (sort of) so I can remember what emacs keyboard shortcuts are in macOS

[Jump to the commands](#Emacs-key-bindings-that-work-in-macOS)

## Introduction

I'm dating myself here, but I started using emacs probably in 1989 or 1990. All through the 90s and early 00s, I used emacs for *everything*. I read my mail and usenet news in it with VM and Gnus, browsed the web in emacs/W3, kept my address book in my editor with BBDB, and used it as my code IDE, web dev environment, and general text editor. I wrote my first few fiction books exclusively in emacs, was a tech editor for the SAMS book _Teach Yourself Emacs_ back in 1999, and helped my longtime friend Bill Perry with the emacs/W3 docs.

I switched from Linux PCs to the Mac in 2005, and by about 2010 or so, I'd moved completely away from emacs. I went with the Mac's built-in programs for mail, web browsing, and addresses. Most of my writing is done in Scrivener. I'm writing this in VSC. I sometimes ponder going back, but I've only got so many hours left on this earth, and can't waste days and weeks unfucking some new change that got introduced by someone in a basement in Norway who decided paragraphs should never start with tabs.

But the keystrokes are still burned into my head. It's like how I can't remember any of my seven phone numbers, but I know that back in 1974, I was at 663-2830. Using <kbd>C-a</kbd> to move to the start of a line is still in my muscle memory. I can never remember how to split a file in VSC (it's <kbd>⌘-K</kbd> <kbd>⌘-\\</kbd>) but I instinctively remember <kbd>C-x 2</kbd>.

I was surprised a few years ago to find that a lot of the key bindings from emacs work in any macOS program. I've seen debate as to why this happened, but I suspect that the Cocoa API is doing this because of it's NeXT lineage. Cocoa is based on what was called Yellow Box during the Rhapsody development as OpenStep was morphed into Mac OS X. And OpenStep was the separation of the OOP APIs of NextStep from the OS layer. What's now macOS (and iOS) is filled with old references to NeXT, like all the classes that are still prefixed with `NS`. 

(I don't know what I am talking about at all and I am not a historian, but here's a conspiracy theory for you: NextStep was primarily developed by Avie Tevanian. I dug around a bit and found a 1985 usenet post from him [here](https://www.tech-insider.org/unix/research/1985/0515.html) from when he was at CMU describing his MicroVAX II/Ultrix setup back then, and he mentions installing emacs. Is that why emacs and not vi key bindings the standard in the NeXT?)

Anyway, enough rambling about my life; this isn't a recipe page, and I don't need to write a thousand words about my grandmother's Polish cooking and my personal journey to find myself before I just tell you what junk to put in the frying pan. (I guess I already did that though, sorry.)

## Emacs key bindings that work in macOS

I'm going to use a lazier version of the Apple convention and say **Cmd**, **Ctrl**, **Opt**, **Shift**, and **Esc**. 

Legend:

* **Command**: the <kbd>⌘</kbd> key.
* **Option**: the <kbd>⌥</kbd> key.
* **Control**: the <kbd>^</kbd> key.
* What emacs calls the **Meta** key is sort of the Mac's **Option** key.
* <sup>*</sup> means something might not work in every program.

### Cursor navigation

Keys to move the cursor/insertion point.

* **Control-a**: Jump to the start of a paragraph.
* **Control-e**: Jump to the end of a paragraph.
* **Control-f**: Jump one character forward.
* **Control-b**: Jump one character backward.
* **Control-l**: Center the cursor or selection in the visible area.<sup>*</sup>
* **Control-p**: Jump up one line.
* **Control-n**: Jump down one line.
* **Option-Left Arrow**: Jump to the beginning of the previous word.
* **Option-Right Arrow**: Jump to the end of the next word.

### Deleting text

Removing text relative to the insertion point.

* **Option-Delete**: Delete the word to the left of the insertion point.
* **Control-h**: Delete the character to the left of the insertion point.
* **Control-d**: Delete the character to the right of the insertion point.
* **Control-k**: Delete everything from the insertion point to the end of the paragraph.

### Editing text

Non-destructive but text-altering commands.

* **Control-t**: Swap the character before the insertion point with the character in after the insertion point.
* **Control-o**: Add a new line after the insertion point.

### What doesn't work

A lot of emacs bindings don't work, but here are the non-operational ones I type the most without thinking.

* **M-** sequences: In emacs, you press Esc, release it, then press something else to do something. For example, M-f will uppercase a word in emacs. In cocoa, the two-step sequence doesn't do anything. **Option-f** at the same time will insert a formula character.
* **Control-x Control-something** sequences: In emacs, a C-x C-t will transpose a line. This two-stroke sequence won't work in Cocoa.
* Mark commands won't work. In emacs, C-SPC starts a mark. Move around, then C-w will delete the region. Cocoa uses the completely different macOS notion of selecting text.
* Search doesn't work. (C-s and C-r)
* **C-u** was a sequence I heavily abused. In emacs, C-u100C-f would repeat C-f 100 times, and move forward 100 characters.
* **Control-g**: the keystroke I type the most im emacs, which is the "stop it and shut the hell up" command. 

### Shell commands

A lot more emacs key bindings work in bash or zsh. This is not a Cocoa or a Mac thing; it's a shell thing. So things like **Control-r** (reverse i-search) or **M-t** (transpose two words). And most importantly, **Control-G** works.
