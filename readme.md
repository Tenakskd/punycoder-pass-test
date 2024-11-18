<p>幸せok改造インスタンス</p>
デプロイボタンは下

## 使い方

右下に出てくる「Cookieを承認しますか？」を承認してください<br>
拒否を押した場合ページをリロードすると再度表示されます。<br>

承認を押すと↓が実行されます。
```JavaScript
document.getElementById('accept-btn').addEventListener('click', function() {
    document.cookie = "yuki=True; max-age=31536000; path=/";
    location.href = "/";
    return;
});
```



## 説明(?)
ASGIで動く、 
blog内に静的サイトを入れると認証されていない時にそのサイトが表示されます。  
cookieにyuki=Trueを設定すると認証されます。  
サーバーの起動時に掲示板の公式インスタンスに接続します。定期的にサーバーを再起動してください。  <br>
<br>
## デプロイ
(slim-2-by-siawaseok.gitがデプロイされます)<br>
<a href="https://render.com/deploy?repo=https://github.com/Tenakskd/punycoder-pass-test">
 <img src="https://render.com/images/deploy-to-render-button.svg" alt="Deploy to Render"><br>
</a>
<a href="https://vercel.com/new/clone?repository-url=https://github.com/tenakskd/punycoder-pass-test.git">
  <img src="https://vercel.com/button" alt="Deployto Vercel">
</a>

[![Deploy to Koyeb](https://www.koyeb.com/static/images/deploy/button.svg)](https://app.koyeb.com/deploy?type=git&builder=buildpack&repository=github.com/tenakskd/punycoder-pass-test&branch=main&name=slim-2-by-siawaseok)
<br>

<h2>偽造ページの変え方</h2>

### はじめに

このリポジトリをフォークしてください。 

次に偽造ページに使いたいhtmlを作ってください

偽造ページを変更するには、以下のファイルを編集します:[blog/index.html](https://github.com/Tenakskd/slim-2-by-siawaseok/main/blog/index.html)


作成した偽造ページのHTML内には、以下のコードが含まれている必要があります。これにより、サイトが正しく機能します。

<img src="IMG_9361.jpeg" width="60%" height="60%">
(これが出てくる様になる)

### 必要なHTML要素

**`<head>`タグに追加する内容:**
```html
<link rel="stylesheet" href="styles.css">
```
**`<body>` タグに追加する内容:**
```html
<div id="cookie-notice" class="cookie-notice">
    このサイトではクッキーを使用しています。<br>
    <button id="accept-btn">承認する</button>
    <button id="reject-btn">拒否する</button>
</div>
<script src="script.js"></script>
```

<br>

### インビのインスタンス
https://docs.invidious.io/instances/<br>
https://invidious.namazso.eu/<br>


