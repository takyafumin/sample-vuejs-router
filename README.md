Vue Routerでのリンク動作サンプル
====================

Nginxのリバースプロキシ構成で, Vue Routerを用いて画面リンク動作を検証する


構成
----------

Appサーバは、Webサーバからproxy_passにて公開されている

```
Browser
    |
    +-- Web(nginx, 80port)
        |
        +-- App(nginx, 80port)
```

機能
----------

|           URL           | アクセス先 |       説明        |
| ----------------------- | ---------- | ----------------- |
| http://localhost/       | Webサーバ  | Home              |
| http://localhost/news1/ | Appサーバ  | news1ページ       |
| http://localhost/news2/ | Appサーバ  | news2ページ       |
| http://localhost/web/   | Webサーバ  | Webサーバのページ |
