import-group-prices
===================

Simple and extensible import tool to allow you to set multiple group prices to magento products!

You can find it in System > Import/Export > Import - Custom

Just import a file with Sku, Customer Group ID, Price -- make sure you include the headers in the first row of the CSV

So for product "ABC", customer group "General" (ID# 1), with price $10.50

``Sku,Group ID,Price``

``ABC,1,10.5``

Install module using composer
=====================

To use composer, firts make sure you have composer installed. 
Read more about installing composer at [getcomposer.org](https://getcomposer.org/)

Setup your project for composer
---

Add a composer.json file to your root dir. Preferable outside the webroot.
Edit the file and add the following to install this module:

composer.json:
```json
{
    "require": {
        "interstroom/import-group-prices": "@dev"
        "magento-hackathon/magento-composer-installer": "*"
    },
    "repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/interstroom/import-group-prices.git"
        }
    ],
    "extra":{
        "magento-root-dir": "http-docs/"
    }
}
```

Make sure the **magento-root-dir** matches your directory in which the magento files (webroot) are located.
The directory structure could look like this:

    the-project-dir/
    ├── composer.json
    └── http-docs/


If you want to use [the public Magento module repository](http://packages.firegento.com),
set up your root ```composer.json``` in your project like this:

```json
{
    "require": {
        "interstroom/import-group-prices": "@dev"
        "magento-hackathon/magento-composer-installer": "*"
    },
    "repositories": [
        {
            "type": "composer",
            "url": "http://packages.firegento.com"
        },
        {
            "type": "vcs",
            "url": "https://github.com/interstroom/import-group-prices.git"
        }
    ],
    "extra":{
        "magento-root-dir": "http-docs/"
    }
}
```

Install the module
---
To install the modules run the `composer install` command. The modules will be downloaded into the vendor directory and symlinked into your magento project.

More information
---
[Magento Composer Installer](https://github.com/magento-hackathon/magento-composer-installer)
