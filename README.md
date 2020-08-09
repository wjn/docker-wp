# Dockerized Wordpress

This repo builds out an instance of wordpress as follows:

- WP 5.4.2
- PHP 7.4
- MySQL 8.0.21

## How to run locally

You must **of course** have docker installed on your local machine.

`docker-compose up` will build out the entire app and start it at `localhost:8080`.

If it's the first time to run, you will need to _install WordPress_ by following the prompts. This will save in the volumes created on your local machine. If you deploy this repo, the data on your machine will not follow over with the exception of anything you have built out in the `wp-content` directory mirrored in the root of this project.

## wp-content

When you install wordpress after spinning up this instance, it will create a mirrored `wp-content` directory in the root of this project. You can then paste in child-themes, uploads, or plugins into that directory following the directory pattern from the WordPress app itself. For example:

```
wp-content
├── plugins
│   ├── PDFEmbedder-premium-secure
│   ├── akismet
│   └── wp-publications-manager
├── themes
│   ├── twentynineteen
│   ├── twentyseventeen
│   ├── twentytwenty
│   └── twentytwenty-child
└── uploads
    ├── 2020
    └── securepdfs
```
