---
title: "Frontier を支える技術"
emoji: "👏"
type: "tech"
topics: ["typescript", "nextjs", "tailwindcss", "prisma", "heroku"]
published: true
---

この記事では、[Frontier](https://frontierjs.herokuapp.com) を作成するにあたって採用した技術について簡単に解説していきます。

## Next.js

[Next.js by Vercel - The React Framework](https://nextjs.org/)

言わずとしれた、React ベースのフレームワークです。間違いなく、Next.js がなければ Frontier は作れなかった･･･とまでは言いませんが、生産性の向上に大きく寄与しているかなと思います。

特に [API Routes](https://nextjs.org/docs/api-routes/introduction) や、[NextAuth.js](https://next-auth.js.org/) が役に立ちました。今回は認証に [Email を用いたマジックリング](https://next-auth.js.org/providers/email) を採用しており、メールの送信には [Mailjet](https://www.mailjet.com/) を利用しています。

この辺に関しては、おいおい詳しい解説記事を書いていく予定です。

## Prisma

[Prisma - Next-generation Node.js and TypeScript ORM for Databases](https://www.prisma.io/)

TypeScript と親和性が鬼のように高い O/R マッパーで、Next.js との相性も抜群です。先ほど触れた API Routes のお陰でそこからエンドポイントを作成して Prisma のクエリを呼び出せますし、NextAuth.js との連携もバッチリです。

## Tailwind CSS

[Tailwind CSS - Rapidly build modern websites without ever leaving your HTML.](https://tailwindcss.com/)

[ユーティリティファースト](https://tailwindcss.jp/docs/utility-first) な CSS フレームワークの代表格である Tailwind CSS を採用しました。

Next.js で書く際は、CSS Modules などを使わずにスタイリングが出来るので開発が非常に楽になって便利ですね（もちろん、CSS Modules と組み合わせることも可能ですが）。

また、今回は Tailwind CSS ベースの CSS フレームワークとして [daisyUI](https://daisyui.com/) を採用しました。daisyUI はスタイリングが Tailwind CSS ベースであるため Tailwind CSS に用意されたクラスでのスタイルの上書きが行いやすく、またテーマなど便利な機能が多数内包されていてとても開発体験が良かったです。

Tailwind CSS の恩恵を受けつつ、デザインを楽したいケースではかなり役立つのではないでしょうか。

## Heroku

[Cloud Application Platform | Heroku](https://www.heroku.com/)

Heroku を使えば DB 環境も用意できるので、今回は Vercel ではなくこちらを採用しました。Heroku 単体でアプリケーションから DB、その他もろもろ面倒を見てくれるのが良いですね。

（この記事の執筆時点では障害が起きていて辛いところがあるのですが 😅）

## おわりに

繰り返しになりますが、各技術の詳細や実際に動いているアプリケーションでの使われ方に関しては、今後さらに記事を書いて解説していく予定なのでお見逃しなく 🙌

---

さいごに、Frontier では一緒にフロントエンドのプロを目指して高め合うコミュニティメンバーを募集しておりますので、以下のページからお気軽にご応募ください ✨

👉 [Frontier（フロンティア） | フロントエンドのプロを目指す学習コミュニティ](https://frontierjs.herokuapp.com/)
