# 😎 Personal Steam Signature Generator

<!-- Remember to change branches in badges after PR to main -->

[![5.3](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP5.3.yml/badge.svg?branch=making-it-modern)](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP5.3.yml)
[![5.4](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP5.4.yml/badge.svg?branch=making-it-modern)](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP5.4.yml)
[![5.6](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP5.6.yml/badge.svg?branch=making-it-modern)](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP5.6.yml)
[![7.0](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP7.0.yml/badge.svg?branch=making-it-modern)](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP7.0.yml)
[![7.4](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP7.4.yml/badge.svg?branch=making-it-modern)](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP7.4.yml)
[![8.0](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP8.0.yml/badge.svg?branch=making-it-modern)](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP8.0.yml)
[![8.4](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP8.4.yml/badge.svg?branch=making-it-modern)](https://github.com/Avaray/personal-steam-signature/actions/workflows/test_PHP8.4.yml)

This [PHP](https://www.php.net/) script generates [PNG](https://en.wikipedia.org/wiki/PNG) image with status of [Steam](https://store.steampowered.com/) user.  
The width of the image adjusts to the length of the username or the length of the game title the user is currently playing. The height of the image is fixed.  
Where you place the generated image is entirely up to you. In the past, people used to add such status images to their signatures on [internet forums](https://en.wikipedia.org/wiki/Internet_forum).

## Requirements

- [PHP](https://www.php.net/) 5.4 or higher. Check badges above for PHP versions.
- [GD](https://github.com/libgd/libgd) extension (version 2.X). Depending on your server configuration, this will either be enabled or disabled. Check this [link](https://stackoverflow.com/questions/2283199/enabling-installing-gd-extension-without-gd) for more information on how to enable it.
- [CURL](https://curl.se/) extension. Same case as with GD extension. If it's not enabled, enable it.

## Installation

1. Clone this repository.

```bash
git clone https://github.com/Avaray/personal-steam-signature.git
```

> soon...

## Usage

There are two ways to configure this script:

1. With `config.php` file.
2. By passing variables as [arguments](https://www.php.net/manual/en/reserved.variables.argv.php). Config file will be ignored if you pass valid arguments.

With [CRON](https://cronitor.io/guides)

> soon...

Remotely with [HTTP Get request](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods/GET)

> soon...

Then you can access your signature with URL like this:

```
https://example.com/path-to-script/76561198037068779.png
```

## Config File

You need `config.php` file only

1. Set `steam_api_key`. You can get it [here](prestashop/github-action-php-lint).
2. Set `steam_id`. You can get it from your Steam profile URL. It's 17 digits long number at the end of the URL. You can use also [this](https://steamid.info/) non-official website to get it.

```php
<?php
return [
    'steam_api_key' => 'XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX',
    'steam_id' => 'XXXXXXXXXXXXXXXXX',
    'capitalized_personaname' => false,
];
```

## # TODO's

- [ ] Re-write the entire script.
- [ ] Auto-creating of `config.php` file if it doesn't exist.
- [ ] Possibility to pass data in URL (use [parse_ur](https://www.php.net/manual/en/function.parse-url.phpl) for that) or as [parameters](https://www.php.net/manual/en/reserved.variables.argv.php).
- [ ] Support for multiple users (up to 100).
- [ ] Workflow for genrating example images.
