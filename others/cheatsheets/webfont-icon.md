# Webfont Icon

## Bootstrap Icons

Official open source SVG icon library for Bootstrap.

- [icons.getbootstrap.com](https://icons.getbootstrap.com/){:target="_blank"}

Bootstrap Icons are published to npm, but they can also be manually downloaded if needed.

```html
<head>
  <!--
    Using dns-prefetch

    DNS-prefetch is an attempt to resolve domain names before resources get requested.
    This could be a file loaded later or link target a user tries to follow.

    https://developer.mozilla.org/en-US/docs/Web/Performance/dns-prefetch
  -->
  <meta http-equiv="x-dns-prefetch-control" content="on">
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
