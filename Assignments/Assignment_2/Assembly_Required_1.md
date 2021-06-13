# PicoGym Web Exploitation Writeup

Author: [Shivam Mishra](https://github.com/7shivamx)

Challenge Page: [Some Assembly Required 1](http://mercury.picoctf.net:37669/index.html)

## Walkthrough
Clicking on the link brought me to a flag validator webpage. Then inspecting the webpage using `Ctrl + Shift + I`, i noticed there was a file named `adda0372` inside  `wasm` folder under source section.
At the bottom of the file, there was the flag.

## Flag
`picoCTF{a8bae10f4d9544110222c2d639dc6de6}`

## Suggested modifications [Optional]
What can you do to make this level more difficult. The inherent idea should be similar.
