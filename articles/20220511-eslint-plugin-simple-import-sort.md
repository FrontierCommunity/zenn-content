---
title: "eslint-plugin-simple-import-sort で import の自動ソートを行う"
emoji: "🔃"
type: "tech"
topics: ["eslint", "nextjs", "javascript"]
published: true
---

[Frontier](https://frontierjs.herokuapp.com) では Next.js を採用しており、ESLint では`eslint-config-next`と`eslint-config-prettier`を利用したシンプルな設定にしていたのですが、`import`の記述を整理するために [eslint-plugin-simple-import-sort](https://github.com/lydell/eslint-plugin-simple-import-sort) を採用することにしました。

## `.eslintrc.json` の記述例

以下は現在プロジェクトで実際に使っている`.eslintrc.json`の内容です。

```json
{
  "extends": ["next/core-web-vitals", "prettier"],
  "plugins": ["simple-import-sort", "import"],
  "rules": {
    "simple-import-sort/imports": "error",
    "simple-import-sort/exports": "error",
    "import/first": "error",
    "import/newline-after-import": "error",
    "import/no-duplicates": "error"
  }
}
```

記述内容は eslint-plugin-simple-import-sort の [README](https://github.com/lydell/eslint-plugin-simple-import-sort#example-configuration) を参考にしています。このシンプルな設定だけで、`import`の順番を自動で整理してくれるのは嬉しいですね。

パッケージの思想としても、シンプルな設定を心がけていることが [README](https://github.com/lydell/eslint-plugin-simple-import-sort#not-for-everyone) から確認できます。複雑な設定が不要で、最低限いい感じの挙動を担保したい場合にうってつけだと思うので、気になる方はぜひ試してみてください ✨
