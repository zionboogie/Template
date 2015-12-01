�E�ŏ����̃e���v���[�g
min_template.html

�Eheader�Anav�Ȃǂ����炩���ߗp��
min_layout_template.html

�Eie9�ȉ��ɂ��Ή�����
lt_ie9.html

�E�p�[�c�W
module.html


�ǂݍ��ރ��Z�b�gCSS��normalize.css�B


## HTML5�ŏ���
``` html
<!DOCTYPE html>
```

## CSS�n�b�N��IE�Ή�
``` html
<!--[if lt IE 7 ]><html class="ie ie6" lang="ja"><![endif]-->
<!--[if IE 7 ]><html class="ie ie7" lang="ja"><![endif]-->
<!--[if IE 8 ]><html class="ie ie8" lang="ja"><![endif]-->
<!--[if (gte IE 9)|!(IE)]><!--><html lang="ja"><!--<![endif]-->
```

## UA�U��
``` html
<meta http-equiv="X-UA-Compatible" content="IE=edge">
```

## viewport
``` html
<meta name="viewport" content="width=device-width, initial-scale=1">
```


<h3>�X�}�z�̕����T�C�Y����</h3>
``` css
body {
	  -webkit-text-size-adjust: 100%;
	}
```

## OGP
``` html
<meta property="og:title" content="�^�C�g��">
<meta property="og:type" content="website">
<meta property="og:url" content="http://�C�ӂ�URL">
<meta property="og:image" content="http://�C�ӂ�URL/og_image.png">
<meta property="og:site_name" content="">
<meta property="og:description" content="" />
<meta property="fb:app_id" content="�C�ӂ�ID">
```

## CSS
``` html
<link rel="stylesheet" href="css/normalize.css">
```


## jQuery�Ή�
<h3>CDN</h3>
``` html
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>
<script> (window.jQuery || document .write('<script src="js/jquery-1.11.2.min.js"><\/script>')); </script>
```

<h3>IE8�ȉ����Ή��������ꍇ</h3>
``` html
<!--[if lt IE 9]>
	<script src="js/html5.js"></script>
	<script src="js/IE9.js"></script>
	<script src="js/css3-mediaqueries.js"></script>
<![endif]-->
```


## role�����ɂ���
role����(�����h�}�[�N����)�Ƃ́AWEB�y�[�W���\������v�f�ɑ΂��Ė���������������̂ŁA�����\���ɑ΂��ڈ�����邱�Ƃ�Web�A�N�Z�V�r���e�B�̌����}�邱�Ƃ��ł��܂��B

�������Ă����̂���₱�����ł����A�Ⴆ��header�v�f�̓y�[�W���ɉ������Ă������ł���ˁB�����Ƌ�̓I�ɂ����΃y�[�W��header�Ƃ��A�R���e���c(section�Ƃ�)���ɂ���header�ł��Brole�����ł���ubanner�v��t�^���邱�ƂŁA�y�[�W��header����Ƃ����悤�ɖ����I�ɖ�����t�^���邱�Ƃ��ł��܂��B


<h3>header</h3>
``` html
<header role="banner">
	<h1>���S</h1>
</header>
```
banner�̓w�b�_�[��\���܂��B��{�I�Ƀy�[�W����1�����ł��B

<h3>nav</h3>
``` html
<nav role="navigation">
	�O���[�o���i�r
</nav>
```
navigation�̓h�L�������g��֘A����h�L�������g�̃i�r�Q�[�V�����������܂��B���Ȃ݂ɁAnav�̓����N�悪��v�ȃy�[�W�̂Ƃ��Ɏg���̂��K�؂Ȃ̂ŁA�O���[�o���i�r�͓��Ă͂܂�܂��ˁB

��������Q�l�ɂ���Ƃ����ł�
<a href="http://html-five.jp/163/" target="_blank">HTML5�̃}�[�N�A�b�v(2) nav�̎g����</a>



<h3>main</h3>
``` html
<main role="main">
	���C���R���e���c
</main>
```
main�̓h�L�������g�̂�����v�ȃR���e���c�������܂��B�y�[�W�� 1 �̂݁B
�Ȃ̂ŁA�h�L�������g��A�v���P�[�V������ body �̃��C���R���e���c��\���Amain�v�f�Ɏg���̂��K�؂ł��ˁB

<h3>aside</h3>
``` html
<aside role="complementary">
	�T�C�h�R���e���c
</aside>
```
complementary�̓h�L�������g��⏕������������܂��Baside���K�؂��Ǝv���܂��B

<h3>footer</h3>
``` html
<footer role="contentinfo">
	�t�b�^�[
</footer>
```

contentinfo�́A�R���e���c�Ɋւ��钘�쌠��v���C�o�V�[���ւ̃����N�������B�y�[�W�� 1 �̂݁B�R�s�[���C�g�Ȃǂ�\������t�b�^�[�������ł��傤�B


## �e���v���[�g
��L�܂Ƃ߂�ƈȉ��̂悤�ɂȂ�܂��B�Ƃ肠�����A���̂Ƃ��낱��Ȃ��񂶂ŗǂ������Ȃ̂ŁA���΂炭�͂���ŁB�����A���̂����X�V����Ǝv���܂��B

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
	<meta property="og:title" content="�^�C�g��">
	<meta property="og:type" content="website">
	<meta property="og:url" content="http://�C�ӂ�URL">
	<meta property="og:image" content="http://�C�ӂ�URL/og_image.png">
	<meta property="og:site_name" content="">
	<meta property="og:description" content="" />
	<meta property="fb:app_id" content="�C�ӂ�ID">
	<title>Document</title>
	<link rel="stylesheet" href="css/normalize.css">
	<link rel="stylesheet" href="css/style.css">
</head>
<body>
	<header role="banner">
		<h1>���S</h1>
	</header>
	<nav role="navigation">
		�O���[�o���i�r
	</nav>
	<main role="main">
		���C���R���e���c
	</main>
	<aside role="complementary">
		�T�C�h�R���e���c
	</aside>
	<footer role="contentinfo">
		�t�b�^�[
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