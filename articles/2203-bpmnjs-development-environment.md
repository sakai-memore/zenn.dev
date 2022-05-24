---
title: "2203-bpmnjs-development-environment"
emoji: "🚝"�"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: []
published: false

---

# 2203-bpmnjs-development-environment

## overview

- bpmn-jsで、modeler, viewerを拡張するにあたり、以下の拡張機能をCustomizeする。
  + Properties Panel
  + Properties Provider
  + Moddle
  + Descripter
  + Overlays
- 拡張機能の実装 implementにあたり、Bundlerを導入する。Bundlerとは、JS Moduleを依存性などを把握して、一つにまとめる機能。
- Bundlerは、viteを採用する。
  + https://vitejs.dev/ 

## environment

```cmd
PS G:\workspace\bpmnplate> node --version
v16.13.0
PS G:\workspace\bpmnplate> npm --version
8.1.0
PS G:\workspace\bpmnplate> npx --version
8.1.0
```

## installation

### nodejs download and installation
- https://nodejs.org/en/download/

### npm install

```cmd
PS G:\workspace\bpmnplate\bpmn-modeler-customed> npm install

up to date, audited 86 packages in 3s

13 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
```


#### package.json

```json
{
  "name": "bpmn-modeler-customed",
  "private": true,
  "version": "0.0.0",
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview",
    "serv": "http-server -o ./index-build.html"
  },
  "devDependencies": {
    "bpmn-js": "^8.10.0",
    "bpmn-js-properties-panel": "^0.46.0",
    "camunda-bpmn-moddle": "^6.1.1",
    "dotenv": "^16.0.0",
    "http-server": "^14.1.0",
    "jquery": "^3.6.0",
    "vite": "^2.8.0"
  }
}

```
## operations

### npm run dev
- `esbuild` を利用して、Cacheに、ES Moduleを展開。dev serverを起動。
  + html, js, cssの修正が即座に反映される

### npm run build
- `rollupjs` を利用して、`dist` directoryにbundleしたjs, cssを配置する。


```cmd
PS G:\workspace\bpmnplate\bpmn-modeler-customed> npm run build

> bpmn-modeler-customed@0.0.0 build
> vite build

vite v2.8.4 building for production...
✓ 1104 modules transformed.
dist/bpmn-modeler-customed.es.js   2186.97 KiB / gzip: 386.98 KiB
dist/bpmn-modeler-customed.umd.js   983.01 KiB / gzip: 269.56 KiB
PS G:\workspace\bpmnplate\bpmn-modeler-customed>
```

### npm run preview
- buildしたCodeの確認用。Entry Pointを、index.html等のhtmlにした場合に動作。（今回は、Entryを、Targetとするjsにするため、利用しない）

### npm run serv
- buildしたjs codeの確認用。http-serverで、index-build.htmlを表示。



