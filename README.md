# .php_version

Easily define aliases on macOS for the most common PHP programs and set default PHP versions for using them.

## Installing different PHP Versions

Use Homebrew to install different versions of PHP

Example: `brew install php@7.4`

## Usage
First you will need to source `.php_versions` from your `.zshrc` file.

### php_path

Next, in your `.zshrc` file, define where each version of php lives using the `php_path` command.

Example:

```bash
php_path 73 "/usr/local/opt/php@7.3/bin/php"
php_path 74 "/usr/local/opt/php@7.4/bin/php"
php_path 80 "/usr/local/opt/php@8.0/bin/php"
```

This will automatically make it so you can use the following commands, suffixed with the version:

- php73
- composer73
- phpunit73
- psysh73
- pecl73

You can replace 73 with whichever version you've defined with `php_path`.

### default_php_version
Set a default PHP version to use by calling  `default_php_version 73` in your `.zshrc`.

After calling this, when you call `php`, `composer`, etc... it will automatically use that version of PHP. You can call this temporarily from your shell to switch in between PHP versions.
