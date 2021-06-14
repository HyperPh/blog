
# npm (nodejs package manager)


## npm安装TypeScript及运行示例

```powershell
PS D:\PowerShell> $env:path+=';F:\lang\js\node-v14.17.0-win-x64;'
PS D:\PowerShell> cd H:\1app\js
PS H:\1app\js> npm install E:\typescript-4.2.4.tgz
npm WARN saveError ENOENT: no such file or directory, open 'H:\1app\js\package.json'
npm notice created a lockfile as package-lock.json. You should commit this file.
npm WARN enoent ENOENT: no such file or directory, open 'H:\1app\js\package.json'
npm WARN js No description
npm WARN js No repository field.
npm WARN js No README data
npm WARN js No license field.

+ typescript@4.2.4
added 1 package from 1 contributor in 2.441s
PS H:\1app\js> H:\1app\js\node_modules\.bin\tsc.ps1 -v
Version 4.2.4
PS H:\1app\js> H:\1app\js\node_modules\.bin\tsc.ps1 E:\hello.ts
PS H:\1app\js> node E:\hello.js
Hello World

```

它还生成了一个好像没什么用的package-lock.json，我删掉了。


```json
{
  "requires": true,
  "lockfileVersion": 1,
  "dependencies": {
    "typescript": {
      "version": "file:E:/typescript-4.2.4.tgz",
      "integrity": "sha512-V+evlYHZnQkaz8TRBuxTA92yZBPotr5H+WhQ7bD3hZUndx5tGOa1fuCgeSjxAzM1RiN5IzvadIXTVefuuwZCRg=="
    }
  }
}

```


## npm创建项目

一个nodejs项目本质上只是一个含有package.json的目录。


```powershell
PS H:\1app\js> npm init
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help init` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (js) nodelib
version: (1.0.0)
description: installed node_modules
entry point: (index.js)
test command: node index.js
git repository: https://github.com/HyperPh/nodelib
keywords: lib
author: PCI
license: (ISC) MIT
About to write to H:\1app\js\package.json:

{
  "name": "nodelib",
  "version": "1.0.0",
  "description": "installed node_modules",
  "main": "index.js",
  "dependencies": {
    "typescript": "^4.2.4"
  },
  "devDependencies": {},
  "scripts": {
    "test": "node index.js"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/HyperPh/nodelib.git"
  },
  "keywords": [
    "lib"
  ],
  "author": "PCI",
  "license": "MIT",
  "bugs": {
    "url": "https://github.com/HyperPh/nodelib/issues"
  },
  "homepage": "https://github.com/HyperPh/nodelib#readme"
}


Is this OK? (yes) yes
PS H:\1app\js>

```

