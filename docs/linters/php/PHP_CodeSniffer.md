# PHP_CodeSniffer

PHP_CodeSniffer tokenizes PHP files and detects violations of a defined set of coding standards.

- [phpcs](https://marketplace.visualstudio.com/items?itemName=ikappas.phpcs){:target="_blank"}
- [github.com/squizlabs/PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer){:target="_blank"}

## Installation

Install PHP_CodeSniffer system-wide with the following command:

```shell
composer global require squizlabs/php_codesniffer
```

Include a dependency for squizlabs/php_codesniffer in your composer.json file.

```shell
composer require --dev squizlabs/php_codesniffer
```

## Configuration

- [Annotated ruleset.xml](https://github.com/squizlabs/PHP_CodeSniffer/blob/master/src/Standards/PSR2/ruleset.xml){:target="_blank"}
- [The Annotated Sample File](https://pear.php.net/manual/en/package.php.php-codesniffer.annotated-ruleset.php){:target="_blank"}

```xml
<?xml version="1.0"?>
<ruleset name="Custom Standard">
    <description>The PSR-2 coding standard.</description>
    <arg name="tab-width" value="4"/>

    <!-- 2. General -->

    <!-- 2.1 Basic Coding Standard -->

    <!-- Include the whole PSR-2 standard -->
    <rule ref="PSR2" />

    <!-- 2.3 Lines -->

    <!-- The soft limit on line length MUST be 120 characters; automated style checkers MUST warn but MUST NOT error at the soft limit. -->
    <rule ref="Generic.Files.LineLength">
        <properties>
            <property name="lineLimit" value="120"/>
            <property name="absoluteLineLimit" value="0"/>
        </properties>
    </rule>
</ruleset>
```

Ignore Line exceeds maximum limit of characters.

```xml
<?xml version="1.0"?>
<ruleset name="Custom Standard">
    <rule ref="Generic.Files.LineLength">
        <exclude name="Generic.Files.LineLength"/>
    </rule>
</ruleset>
```

## Integration with visual studio code

Install through vscode extensions. Search for [phpcs](https://marketplace.visualstudio.com/items?itemName=ikappas.phpcs){:target="_blank"}.

**settings.json**

Enable/disable built-in PHP validation.

```json
{
    "php.validate.enable": false,
}
```

Controls whether the built-in PHP language suggestions are enabled. The support suggests PHP globals and variables.

```json
{
    "php.suggest.basic": false,
}
```

Control whether phpcs is enabled for PHP files or not.

```json
{
    "phpcs.enable": true,
}
```

Optional. The name or path of the coding standard to use. Defaults to the one set in phpcs global config.

```json
{
    "phpcs.standard": "PSR2",
}
```

Automatically search for any `phpcs.xml`, `phpcs.xml.dist`, `phpcs.ruleset.xml` or `ruleset.xml` file to use as configuration. Overrides custom standards defined above.

```json
{
    "phpcs.autoConfigSearch": true,
}
```
