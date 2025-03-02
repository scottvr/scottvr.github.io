---
title: "Announcing ASCop!"
date: 2025-02-28
---

# ASCop 
[A Case (and Remedy) Against Unsolicited Smart Punctuation](https://github.com/scottvr/ascop/)

### The Principle of Least Astonishment (POLA)

When I input text via keyboard, or on a software version of one displayed on my iPhone that even has enhanced long-press optional variants of these characters (should those non-ASCII characters be what I actually want) I expect the exact characters I typed to be preserved in the document to which I introduce them. 

The automatic substitution of a minus (-) with an emdash (—), a single quote (') with a curly apostrophe (’), or a simple double quote (") with a typographically "correct" quotation mark (“ or ”), or perhaps my [least] favorite: if I type three dots, full stops, periods, or decimal points - ASCII 0x2E - I want ..., not … (…) These are violations of POLA because I never explicitly asked for those substitutions. These unwanted changes also eschew WYSIWYG and DWIM.

Of course what proves to be astonishing to one type of user may be as different as another user and use cases themselves, and a company creating software for profit will generally aim to serve whichever class of users is the majority, targeting niche markets notwithstanding.

### The Problem With Smart Punctuation

For many people, having their software (such as a word processor) act as an editor and typesetter is a beneficial feature, as it saves them time they would otherwise have to spend on re-formatting. However, the insidious creeping presence into note-taking apps, text messages, and other spaces where it could be sensibly assumed one could get an actual plain-text export means that what is actually typed is often not what one gets when copy-pasting or otherwise sending the text elsewhere. This is problematic, for example when:

- Sending code snippets where an emdash breaks syntax. (your programming language probably expects single and double ticks, not “ (&ldquo;) and ” (&rdquo;) surrounding strings.)
- Writing a list of commands, intending to paste them into a terminal to be parsed by a shell, where ticks and backticks have special meanings, and a fancy apostrophe causes errors.
- Writing a plaintext file that you should be able to expect to be portable across systems.
- Using SMS or simple messaging apps, or even HTML form fields where unexpected characters may break formatting.

### Existing Tools Too Much or Not Enough

[Read more about it or download it at my GitHub repo](https://github.com/scottvr/ascop/)
