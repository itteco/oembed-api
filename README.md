# oEmbed API for open-source projects and embeds publishers

[Iframely](https://iframely.com) makes an open embeds API available for the use in your open-source project. Or, if you publish embeds, this open API can present your embeds to be discovered by developers via [oEmbed](http://oembed.com) protocol. 

## For your open-source project

So you need embeds for your open-source project. [oEmbed](http://oembed.com) is great fit. There are many solutions available, including open-source solutions or commercial APIs. Say, [Iframely parsers](https://github.com/itteco/iframely) and [Iframely cloud](https://iframely.com) to mention a few. 

oEmbed protocols make it possible for users of your open-source package to switch between implementations with ease, just by changing API endpoint address. So you don’t lock them down if you go with oEmbed. However, you do need a default endpoint to put it in your box. 

To help you out, we make the two endpoints open, free and public (no API keys):

oEmbed API: 
[>> http://open.iframe.ly/oembed?url=…. & origin=…](http://open.iframe.ly/api/oembed?url=http://vimeo.com/62092214&origin=)

Iframely API:
[>> http://open.iframe.ly/iframely?url=…. & origin=…](http://open.iframe.ly/api/iframely?url=http://vimeo.com/62092214&origin=)

Where `url` is URL-encoded and `origin` should contain a string with either your GitHub username or your Twitter @handle (which is perhaps the same for most of you).  

More request parameters are available too. [See docs](https://iframely.com/docs).

The embed codes will be responsive whenever possible, will cover all our 1600+ domains, will provide [Summary Cards](https://iframely.com/docs/widgets) for the other links. Plus CORS and JSONP so that you can call API with your JavaScript code. 

## For your site

If you publish Twitter Cards or Open Graph, Iframely can also convert those into [oEmbed](http://oembed.com) so that you publish to developers who auto-discover  oEmbed.

For it, you just add the following markup into `<head>` section of your page:

		<link rel="alternate" href="http://open.iframe.ly/api/oembed?url=...&origin=..." type="application/json+oembed"/>
		<link rel="alternate" href="http://open.iframe.ly/api/oembed?url=...&origin=...&format=xml" type="application/xml+oembed"/>

Where `url` is URL-encoded and `origin` should contain a string with either your GitHub username or your Twitter @handle (which is perhaps the same for most of you).

Twitter players, photos and Open Graph videos work best. [Debug your URLs](http://iframely.com/domain) and [whitelist your domain](https://iframely.com/qa/request) for proper coverage. Otherwise, Iframely will generate a [summary card](https://iframely.com/docs/widgets). Contact us if you need a custom parser for your embeds.


## Terms

* The open API endpoints are powered by Iframely cloud and have the same uptime guarantee. 
* However, these are free for open-source and non-commercial use only.
* In your open-source project, make the endpoint address a config variable so that your users can re-configure it to point to any of oEmbed gateway of their choosing when they start using it.
* Mention the fact that they need to configure oEmbed API endpoint in your README file or where appropriate. 
* Be nice. We reserve the right to rate-limit or block IP addresses. No rate-limit is there by default (we presume innocence). So, 
* Make sure we can contact you in case of an issue. Based on your `origin` value, if your GitHub profile doesn’t list an email address, please, consider following [Iframely on Twitter](https://twitter.com/iframely) so we can send a direct message. 

* Last, but not least - fork [this document on GitHub](https://github.com/itteco/oembed-api) and pull-request with the link to your open-source project.

## Implementations:

* [CKEditor](https://github.com/ckeditor/ckeditor-dev) text editor 
* [Medium Insert](https://github.com/orthes/medium-editor-insert-plugin) plugin for [MediumEditor](https://github.com/daviferreira/medium-editor)
* [hypeEmbed](https://github.com/hypeJunction/hypeEmbed) plugin for Elgg community software
* Iframely for [WordPress](https://wordpress.org/plugins/iframely)