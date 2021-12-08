---
title: "2112-vscode-setting"
emoji: "🎹"
type: "tech"
topics: ["vscode"]
published: false
---
# 2112-vscode-setting
## overview
- VS Code for development setting
## download
- https://code.visualstudio.com/Download

## features
- Intellisense
  - 各Language Serviceで、言語ごとにSmartなコード補完ができるようになっている。
  - 型推論により、変数などの型誤りに、警告が表示される
- Code jump
  - 定義個所に、jumpできる。

## installation
-
 ![install options](https://i.gyazo.com/5742d213f35d7d009800944a61ae1a1e.png)
## VS Code features
### The Fundamentals
- Multi-cursor Editing
- **IntelliSense**
- Line Action
  - Copy a line and insert it above or below the current position with `shift+alt+↓` or `shift+alt+↑` respectively.
  - Move an entire line or selection of lines up or down with `alt+↑` or `alt+↓` respectively.
  - Delete the entire line with `ctrl+shift+K`
  - Comment out a block of coe with `ctrl+/`- you can toggle commenting by pressing it. 
- Rename Refactoring: `F2`
  - VS Code's intellisense uses JSDoc comments to provide richer suggestions. The type and documentation from JSDoc comments show up when you hover over a reference to Class or in intelliSense whtn you create a new instance of Class.
- Formatting
  - `shift+Alt+F`: 
  - `ctrl+k`, `ctrl+f: `
- Code Folding
  - `ctrl+shift+[`, `ctrl+shift+]`
  - To fold all sections use `ctrl+K`
  - To unfold all sections use `ctrl+J`
- Errors and Warnings
  - `F8`
- Snippets
  - 
- **Emmet**
```
ul>li.item*5
```

- **Javascript Type Checking**
  - Type-checking your js code can help you spot mistakes you might have not caught otherwise. You can run the Typescript type checker against your existing js code by simply adding a `// @ts-check` comment to the top of your file.

## typescript
- 