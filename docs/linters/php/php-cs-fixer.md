# PHP-CS-Fixer

- [cs.symfony.com/](https://cs.symfony.com/){:target="_blank"}
- [github.com/FriendsOfPHP/PHP-CS-Fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer){:target="_blank"}

## Installation

The recommended way to install PHP CS Fixer is to use Composer in a dedicated composer.json file in your project.

```shell
composer require --dev friendsofphp/php-cs-fixer
```

## Configuration

config file .php-cs-fixer.php example.

```php
<?php

return (new PhpCsFixer\Config())
    ->setRules([
        '@PSR2'                                  => true,
        'array_indentation'                      => true,
        'array_syntax'                           => ['syntax' => 'short'],
        'combine_consecutive_unsets'             => true,
        'class_attributes_separation'            => ['elements' => ['method' => 'one', ]],
        'multiline_whitespace_before_semicolons' => false,
        'single_quote'                           => true,

        'binary_operator_spaces' => [
            'operators' => [
                // '=>' => 'align',
                // '=' => 'align'
            ]
        ],
        // 'blank_line_after_opening_tag' => true,
        // 'blank_line_before_statement' => true,
        'braces' => [
            'allow_single_line_closure' => true,
        ],
        // 'cast_spaces' => true,
        // 'class_definition' => array('singleLine' => true),
        'concat_space'              => ['spacing' => 'one'],
        'declare_equal_normalize'   => true,
        'function_typehint_space'   => true,
        'single_line_comment_style' => ['comment_types' => ['hash']],
        'include'                   => true,
        'lowercase_cast'            => true,
        // 'native_function_casing' => true,
        // 'new_with_braces' => true,
        // 'no_blank_lines_after_class_opening' => true,
        // 'no_blank_lines_after_phpdoc' => true,
        'no_blank_lines_before_namespace' => true,
        // 'no_empty_comment' => true,
        // 'no_empty_phpdoc' => true,
        // 'no_empty_statement' => true,
        'no_extra_blank_lines' => [
            'tokens' => [
                'curly_brace_block',
                'extra',
                // 'parenthesis_brace_block',
                // 'square_brace_block',
                'throw',
                'use',
            ]
        ],
        // 'no_leading_import_slash' => true,
        // 'no_leading_namespace_whitespace' => true,
        // 'no_mixed_echo_print' => array('use' => 'echo'),
        'no_multiline_whitespace_around_double_arrow' => true,
        // 'no_short_bool_cast' => true,
        // 'no_singleline_whitespace_before_semicolons' => true,
        'no_spaces_around_offset' => true,
        // 'no_trailing_comma_in_list_call' => true,
        // 'no_trailing_comma_in_singleline_array' => true,
        // 'no_unneeded_control_parentheses' => true,
        // 'no_unused_imports' => true,
        'no_whitespace_before_comma_in_array' => true,
        'no_whitespace_in_blank_line'         => true,
        // 'normalize_index_brace' => true,
        'object_operator_without_whitespace' => true,
        // 'php_unit_fqcn_annotation' => true,
        // 'phpdoc_align' => true,
        // 'phpdoc_annotation_without_dot' => true,
        // 'phpdoc_indent' => true,
        // 'phpdoc_inline_tag' => true,
        // 'phpdoc_no_access' => true,
        // 'phpdoc_no_alias_tag' => true,
        // 'phpdoc_no_empty_return' => true,
        // 'phpdoc_no_package' => true,
        // 'phpdoc_no_useless_inheritdoc' => true,
        // 'phpdoc_return_self_reference' => true,
        // 'phpdoc_scalar' => true,
        // 'phpdoc_separation' => true,
        // 'phpdoc_single_line_var_spacing' => true,
        // 'phpdoc_summary' => true,
        // 'phpdoc_to_comment' => true,
        // 'phpdoc_trim' => true,
        // 'phpdoc_types' => true,
        // 'phpdoc_var_without_name' => true,
        // 'increment_style' => true,
        // 'return_type_declaration' => true,
        // 'self_accessor' => true,
        // 'short_scalar_cast' => true,
        // 'single_blank_line_before_namespace' => true,
        // 'single_class_element_per_statement' => true,
        // 'space_after_semicolon' => true,
        // 'standardize_not_equals' => true,
        'ternary_operator_spaces' => true,
        // 'trailing_comma_in_multiline_array' => true,
        'trim_array_spaces'               => true,
        'unary_operator_spaces'           => true,
        'whitespace_after_comma_in_array' => true,
        'space_after_semicolon'           => true,
        // 'single_blank_line_at_eof' => false
    ])
    // ->setIndent("\t")
    ->setLineEnding("\n")
;
```

## Integration with visual studio code

Install through vscode extensions. Search for [php cs fixer](https://marketplace.visualstudio.com/items?itemName=junstyle.php-cs-fixer){:target="_blank"}.

**settings.json**

```json
{
    "php-cs-fixer.onsave": true,
    "php-cs-fixer.rules": "@PSR2",
    "php-cs-fixer.autoFixByBracket": true,
    "php-cs-fixer.autoFixBySemicolon": false,
    "php-cs-fixer.formatHtml": false,

    "[php]": {
        "editor.defaultFormatter": "junstyle.php-cs-fixer",
        "editor.tabSize": 4,
        "editor.formatOnSave": true
    },
}
```

Configure php-cs-fixer to execute on save.

```json
{
    "php-cs-fixer.onsave": true,
}
```

PHP CS Fixer level setting (`@PSR1`, `@PSR2`, `@Symfony`).

```json
{
    "php-cs-fixer.rules": "@PSR2",
}
```

When press down the key } auto fix the code in the brackets {}.

```json
{
    "php-cs-fixer.autoFixByBracket": true,
}
```

When press down the key ; auto fix the code at the current line.

```json
{
    "php-cs-fixer.autoFixBySemicolon": false,
}
```

Whether formatting html at the same time.

```json
{
    "php-cs-fixer.formatHtml": false,
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
