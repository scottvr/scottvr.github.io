---
title: "Announcing ASCop!"
date: 2025-02-28
---

# ASCop 
[A Case (and Remedy) Against Unsolicited Smart Punctuation](https://github.com/scottvr/ascop/)

### The Principle of Least Astonishment (POLA)
... The automatic substitution of a minus (-) with an emdash (—), a single quote (') with a curly apostrophe (’), or a simple double quote (") with a typographically “correct” quotation mark (“ or ”) is a violation of [POLA](https://en.wikipedia.org/wiki/Principle_of_least_astonishment) because I never explicitly asked for those substitutions.

### The Problem With Smart Punctuation
... what is assumed to be a *plain-text* export is often not what I get when I copy-paste or send the text elsewhere. I am often having to spend time editing text to undo these unwanted substitutions.

- Sending code snippets where an emdash breaks syntax. (your programming language probably expects single and double ticks, not &ldquo; (`&ldquo;`) and &rdquo; (`&rdquo;`) surrounding strings.)
- Writing a list of command, intending to paste them into a terminal to be parsed by a shell, where ticks and backticks have special meanings, and a fancy apostrophe causes errors.
- Writing a plaintext file that you should be able to expect to be portable across systems.
- Using SMS or simple messaging apps, or even HTML form fields where unexpected characters may break formatting.
   - (and if you're like me and often need to compose your long body of text outside of an app prone to crashing, refreshing, or otherwise finding ways to lose a whole bunch of typing you've done with no way to recover it, finding that when you paste the long-form text into the shaky input are, you break it anyway with some uninvited text your editor has "helpfully" swapped in for you.)
- Oh, how could I have forgotten to mention in the preface perhaps my favorite of them all. If I type three dots, full stops, periods, or decimal points - ASCII 0x2E - I want `...`, not &mldr; (`&mldr;`)

### Existing Tools Too Much or Not Enough

[Read more about it or download it at my GitHub repo](https://github.com/scottvr/ascop/)
