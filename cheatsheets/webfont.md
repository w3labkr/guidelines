# Web Font

## Web Font Loader

Web Font Loader gives you added control when using linked fonts via @font-face.

[github.com/typekit/webfontloader](https://github.com/typekit/webfontloader){:target="_blank"}

You could load fonts from Google Fonts using the Web Font Loader hosted on Google Hosted Libraries using the following code.

```html
<head>
  <meta http-equiv="x-dns-prefetch-control" content="on">
  
  <!--
    Using dns-prefetch

    DNS-prefetch is an attempt to resolve domain names before resources get requested.
    This could be a file loaded later or link target a user tries to follow.

    https://developer.mozilla.org/en-US/docs/Web/Performance/dns-prefetch
  -->
  <link rel="preconnect" href="https://ajax.googleapis.com" crossorigin>
  <link rel="dns-prefetch" href="https://ajax.googleapis.com">
</head>
<body>
  ...
  
  <script src="https://ajax.googleapis.com/ajax/libs/webfont/1.6.26/webfont.js"></script>
</body>
```

To use the Web Font Loader library, just include it in your page and tell it which fonts to load.

```html
<script>
var WebFontConfig = {
    google: {
      families: ['Noto Sans KR:100,400,700'],
      text: ' !"#$%&\'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`abcdefghijklmnopqrstuvwxyz{|}~'
    }
  };
  WebFont.load(WebFontConfig);
</script>
```

## Web Font Icons

### Bootstrap Icons

Official open source SVG icon library for Bootstrap.

[icons.getbootstrap.com/](https://icons.getbootstrap.com/){:target="_blank"}

Bootstrap Icons are published to npm, but they can also be manually downloaded if needed.

```html
<head>
  <meta http-equiv="x-dns-prefetch-control" content="on">
  
  <!--
    Using dns-prefetch

    DNS-prefetch is an attempt to resolve domain names before resources get requested.
    This could be a file loaded later or link target a user tries to follow.

    https://developer.mozilla.org/en-US/docs/Web/Performance/dns-prefetch
  -->
  <link rel="preconnect" href="https://cdn.jsdelivr.net" crossorigin>
  <link rel="dns-prefetch" href="https://cdn.jsdelivr.net">
  
  <!--
    Bootstrap Icons
    Official open source SVG icon library for Bootstrap.
    
    https://icons.getbootstrap.com/
  -->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.8.1/font/bootstrap-icons.css">
</head>
```

Icon fonts with classes for every icon are also included for Bootstrap Icons.

```html
<i class="bi bi-123"></i>
```
