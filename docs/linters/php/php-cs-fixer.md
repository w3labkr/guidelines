# PHP-CS-Fixer

- [cs.symfony.com/](https://cs.symfony.com/){:target="_blank"}
- [github.com/FriendsOfPHP/PHP-CS-Fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer){:target="_blank"}

## Installation

The recommended way to install PHP CS Fixer is to use Composer in a dedicated composer.json file in your project.

```shell
composer require --dev friendsofphp/php-cs-fixer
```

## Integration with visual studio code

Install through vscode extensions. Search for [php cs fixer](https://marketplace.visualstudio.com/items?itemName=junstyle.php-cs-fixer){:target="_blank"}.

**settings.json**

PHP CS Fixer level setting (@PSR1, @PSR2, @Symfony).

```json
{
    "php-cs-fixer.rules": "@PSR2",
}
```

Configure settings to be overridden for the php language.

```json
{
    "[php]": {
        "editor.defaultFormatter": "junstyle.php-cs-fixer",
        "editor.tabSize": 4,
        "editor.formatOnSave": true
    },
}
```
