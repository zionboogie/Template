・最小限のテンプレート
min_template.html

・header、navなどをあらかじめ用意
min_layout_template.html

・min_layout_template.htmlをベースにSass対応
min_layout_sass_template.html

・ie9以下にも対応する
lt_ie9.html

・パーツ集
module.html



読み込むリセットCSSはhtml5doctor
<<<<<<< .mine


## HTML5で書く
``` html
<!DOCTYPE html>
```

## CSSハックでIE対応
``` html
<!--[if lt IE 7 ]><html class="ie ie6" lang="ja"><![endif]-->
<!--[if IE 7 ]><html class="ie ie7" lang="ja"><![endif]-->
<!--[if IE 8 ]><html class="ie ie8" lang="ja"><![endif]-->
<!--[if (gte IE 9)|!(IE)]><!--><html lang="ja"><!--<![endif]-->
```

## ユーザーエージェントの偽装
``` html
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

## viewport
``` html
<meta name="viewport" content="width=device-width, initial-scale=1">
```


<h3>スマホの文字サイズ調整</h3>
``` css
body {
	  -webkit-text-size-adjust: 100%;
	}
```

## OGP
``` html
<meta property="og:title" content="タイトル">
<meta property="og:type" content="website">
<meta property="og:url" content="http://任意のURL">
<meta property="og:image" content="http://任意のURL/og_image.png">
<meta property="og:site_name" content="">
<meta property="og:description" content="" />
<meta property="fb:app_id" content="任意のID">
```

## CSS
``` html
<link rel="stylesheet" href="css/normalize.css">
<link rel="stylesheet" href="css/reset.css">
```


## jQuery対応
<h3>CDN</h3>
``` html
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>
<script> (window.jQuery || document .write('<script src="js/jquery-1.11.2.min.js"><\/script>')); </script>
```

<h3>IE8以下も対応したい場合</h3>
``` html
<!--[if lt IE 9]>
	<script src="js/html5.js"></script>
	<script src="js/IE9.js"></script>
	<script src="js/css3-mediaqueries.js"></script>
<![endif]-->
```


## role属性について
role属性(ランドマーク属性)とは、WEBページを構成する要素に対して役割を持たせるもので、文書構造に対し目印をつけることでWebアクセシビリティの向上を図ることができます。

役割っていうのがややこしいですが、例えばheader要素はページ内に何個あってもいいですよね。もっと具体的にいえばページのheaderとか、コンテンツ(sectionとか)内にあるheaderです。role属性である「banner」を付与することで、ページのheaderだよというように明示的に役割を付与することができます。


<h3>header</h3>
``` html
<header role="banner">
	<h1>ロゴ</h1>
</header>
```
bannerはヘッダーを表します。基本的にページ内で1個だけです。

<h3>nav</h3>
``` html
<nav role="navigation">
	グローバルナビ
</nav>
```
navigationはドキュメントや関連するドキュメントのナビゲーションを示します。ちなみに、navはリンク先が主要なページのときに使うのが適切なので、グローバルナビは当てはまりますね。

こちらを参考にするといいです
<a href="http://html-five.jp/163/" target="_blank">HTML5のマークアップ(2) navの使い方</a>



<h3>main</h3>
``` html
<main role="main">
	メインコンテンツ
</main>
```
mainはドキュメントのうち主要なコンテンツを示します。ページに 1 つのみ。
なので、ドキュメントやアプリケーションの body のメインコンテンツを表す、main要素に使うのが適切ですね。

<h3>aside</h3>
``` html
<aside role="complementary">
	サイドコンテンツ
</aside>
```
complementaryはドキュメントを補助する情報を示します。asideが適切だと思います。

<h3>footer</h3>
``` html
<footer role="contentinfo">
	フッター
</footer>
```

contentinfoは、コンテンツに関する著作権やプライバシー情報へのリンクを示す。ページに 1 つのみ。コピーライトなどを表示するフッターがいいでしょう。


## テンプレート
上記まとめると以下のようになります。とりあえず、今のところこんなかんじで良さそうなので、しばらくはこれで。多分、そのうち更新すると思います。

``` html
<!DOCTYPE html>
<!--[if lt IE 7 ]><html class="ie ie6" lang="ja"><![endif]-->
<!--[if IE 7 ]><html class="ie ie7" lang="ja"><![endif]-->
<!--[if IE 8 ]><html class="ie ie8" lang="ja"><![endif]-->
<!--[if (gte IE 9)|!(IE)]><!--><html lang="ja"><!--<![endif]-->
<head>
	<meta charset="utf-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<meta name="description" content="">
	<meta name="keywords" content="">
	<meta property="og:title" content="タイトル">
	<meta property="og:type" content="website">
	<meta property="og:url" content="http://任意のURL">
	<meta property="og:image" content="http://任意のURL/og_image.png">
	<meta property="og:site_name" content="">
	<meta property="og:description" content="" />
	<meta property="fb:app_id" content="任意のID">
	<title>Document</title>
	<link rel="stylesheet" href="css/normalize.css">
	<link rel="stylesheet" href="css/style.css">
</head>
<body>
	<header role="banner">
		<h1>ロゴ</h1>
	</header>
	<nav role="navigation">
		グローバルナビ
	</nav>
	<main role="main">
		メインコンテンツ
	</main>
	<aside role="complementary">
		サイドコンテンツ
	</aside>
	<footer role="contentinfo">
		フッター
	</footer>

	<script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>
	<script> (window.jQuery || document .write('<script src="js/jquery-1.11.2.min.js"><\/script>')); </script>

	<!--[if lt IE 9]>
		<script src="js/html5.js"></script>
		<script src="js/IE9.js"></script>
		<script src="js/css3-mediaqueries.js"></script>
	<![endif]-->

</body>
</html>
```

``` css
body {
	-webkit-text-size-adjust: 100%;
}
```
=======
test3



>>>>>>> .theirs
