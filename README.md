# Gatsby WordPress inline images

`gatsby-source-wordpress` doesn't process images in blocks of text which means your admin site has to serve the images. This plugin solves that.

Require `gatsby-source-wordpress` and `gatsby-image` to be preinstalled

This repo is forked from `gatsby-wordpress-inline-images` by ([@TylerBarnes](https://github.com/TylerBarnes)) and from now on I am going to maintain this repo.

## installation

```bash
yarn add @draftbox-co/gatsby-wordpress-inline-images
```

Add this plugin as a plugin of `gatsby-source-wordpress`.
Be sure to specify your baseurl and protocol a second time in the `gatsby-wordpress-inline-images` options, not just in the `gatsby-source-wordpress` options.

```javascript
  {
    resolve: `gatsby-source-wordpress`,
    options: {
      baseUrl: `your-site.com`
      protocol: `https`,
      plugins: [
          {
            resolve: `@draftbox-co/gatsby-wordpress-inline-images`,
            options: {
              baseUrl: `your-site.com`,
              protocol: `https`
            }
          }
        ]
      }
  }
```

## Options

```javascript
{
	resolve: `gatsby-source-wordpress`,
	options: {
		// required
		baseUrl: `your-site.com`,
		protocol: `https`,
		// defaults
		maxWidth: 650,
		wrapperStyle: ``,
		postTypes: ["post", "page"],
		backgroundColor: `white`,
		withWebp: false, // enable WebP files generation
		useACF: false, // process <img> tags in ACF fields too
		// add any image sharp fluid options here
		// ...
	}
}
```

## Contributions
PRs are welcome! Consider contributing to this project if you are missing feature that is also useful for others.

# Copyright & License

Copyright (c) 2020 [Draftbox](https://draftbox.co) - Released under the [MIT license](LICENSE).
