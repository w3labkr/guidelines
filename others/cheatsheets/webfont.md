# Webfont

## Webfont Loader

Web Font Loader gives you added control when using linked fonts via @font-face.

- [github.com/typekit/webfontloader](https://github.com/typekit/webfontloader){:target="_blank"}

You could load fonts from Google Fonts using the Web Font Loader hosted on Google Hosted Libraries using the following code.

```html
<script src="https://ajax.googleapis.com/ajax/libs/webfont/1.6.26/webfont.js"></script>
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

## Bootstrap Icons

Official open source SVG icon library for Bootstrap.

- [icons.getbootstrap.com](https://icons.getbootstrap.com/){:target="_blank"}

Bootstrap Icons are published to npm, but they can also be manually downloaded if needed.

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.8.1/font/bootstrap-icons.css">
```

Icon fonts with classes for every icon are also included for Bootstrap Icons.

```html
<i class="bi bi-123"></i>
```
