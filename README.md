# WP Offload S3 Pro Installer


A composer plugin that makes installing [WP Offload S3 Pro] with [composer] easier.

It reads your :key: WP Offload S3 key from the **environment** or a **.env file**.

[WP Offload S3]: https://deliciousbrains.com/wp-offload-s3/
[composer]: https://github.com/composer/composer

## Usage

**1. Add the package repository to the [`repositories`][composer-repositories] field in `composer.json` 
   (based on this [gist][package-gist]):**

```json
    {
      "type": "package",
      "package": {
        "name": "deliciousbrains/wp-offload-s3-pro",
        "type": "wordpress-plugin",
        "version": "1.1.6",
        "dist": {
          "type": "zip",
          "url": "https://deliciousbrains.com/dl/wp-offload-s3-pro-latest.zip?"
        },
        "require": {
          "intelligence/wpos-pro-installer": "^1.0.7",
          "composer/installers": "^1.0"
        }
      }
    },
    {
      "type": "package",
      "package": {
        "name": "deliciousbrains/wp-offload-s3-assets",
        "type": "wordpress-plugin",
        "version": "1.2",
        "dist": {
          "type": "zip",
          "url": "https://deliciousbrains.com/dl/wp-offload-s3-assets-latest.zip?"
        },
        "require": {
          "intelligence/wpos-pro-installer": "^1.0.7",
          "composer/installers": "^1.0"
        }
      }
    },
    {
      "type": "package",
      "package": {
        "name": "deliciousbrains/wp-offload-s3-edd",
        "type": "wordpress-plugin",
        "version": "1.0.4",
        "dist": {
          "type": "zip",
          "url": "https://deliciousbrains.com/dl/wp-offload-s3-edd-latest.zip?"
        },
        "require": {
          "intelligence/wpos-pro-installer": "^1.0.7",
          "composer/installers": "^1.0"
        }
      }
    },
    {
      "type": "package",
      "package": {
        "name": "deliciousbrains/wp-offload-s3-woocommerce",
        "type": "wordpress-plugin",
        "version": "1.0.5",
        "dist": {
          "type": "zip",
          "url": "https://deliciousbrains.com/dl/wp-offload-s3-woocommerce-latest.zip?"
        },
        "require": {
          "intelligence/wpos-pro-installer": "^1.0.7",
          "composer/installers": "^1.0"
        }
      }
    },
    {
      "type": "package",
      "package": {
        "name": "deliciousbrains/wp-offload-s3-enable-media-replace",
        "type": "wordpress-plugin",
        "version": "1.0.1",
        "dist": {
          "type": "zip",
          "url": "https://deliciousbrains.com/dl/wp-offload-s3-enable-media-replace-latest.zip?"
        },
        "require": {
          "intelligence/wpos-pro-installer": "^1.0.7",
          "composer/installers": "^1.0"
        }
      }
    },
    {
      "type": "package",
      "package": {
        "name": "deliciousbrains/wp-offload-s3-meta-slider",
        "type": "wordpress-plugin",
        "version": "1.0.1",
        "dist": {
          "type": "zip",
          "url": "https://deliciousbrains.com/dl/wp-offload-s3-meta-slider-latest.zip?"
        },
        "require": {
          "intelligence/wpos-pro-installer": "^1.0.7",
          "composer/installers": "^1.0"
        }
      }
    },
    {
      "type": "package",
      "package": {
        "name": "deliciousbrains/wp-offload-s3-wpml",
        "type": "wordpress-plugin",
        "version": "1.0.1",
        "dist": {
          "type": "zip",
          "url": "https://deliciousbrains.com/dl/wp-offload-s3-wpml-latest.zip?"
        },
        "require": {
          "intelligence/wpos-pro-installer": "^1.0.7",
          "composer/installers": "^1.0"
        }
      }
    },
    {
      "type": "package",
      "package": {
        "name": "deliciousbrains/wp-offload-s3-acf-image-crop",
        "type": "wordpress-plugin",
        "version": "1.0",
        "dist": {
          "type": "zip",
          "url": "https://deliciousbrains.com/dl/wp-offload-s3-acf-image-crop-latest.zip?"
        },
        "require": {
          "intelligence/wpos-pro-installer": "^1.0.7",
          "composer/installers": "^1.0"
        }
      }
    }
```
Replace `"version": "*.*.*"` with your desired version.

**2. Make your WP Offload S3 key available**

Set the environment variable **`WPOS_PRO_KEY`** to your WP Offload S3 key.

Alternatively you can add an entry to your **`.env`** file:

```ini
# .env (same directory as composer.json)
WPOS_PRO_KEY=Your-Key-Here
```

**3. Require WP Offload S3**

```sh
composer require deliciousbrains/wp-offload-s3-pro:*
```
Unfortunately, DeliciousBrains is not exposing a way of retrieving different versions of their plugin.
Because of this, changing the version in the package section will download the latest version regardless.
You have to manually change the version in your `composer.json` file to manually trigger composer to download a new package.
[composer-repositories]: https://getcomposer.org/doc/04-schema.md#repositories
[composer-versions]: https://getcomposer.org/doc/articles/versions.md
[package-gist]: https://gist.github.com/dmalatesta/4fae4490caef712a51bf
[wpos-account]: https://deliciousbrains.com/signin/
