## For your open-source project

[oEmbed](http://oembed.com) is a great fit if you need embeds. It is an open standard and many solutions exist. Open-source or commercial ones. Say, [Iframely open-source](https://github.com/itteco/iframely) and [Iframely hosted](https://iframely.com), to mention a few :)

Since many oEmbed options are available, it will be possible for users of your open-source package to switch between proxy implementations with ease, just by changing API endpoint address. Basically, you don’t limit them if you go with oEmbed. They can even develop their own proxy API and still be connected. 

However, you do need a default proxy endpoint to put it in your settings. Here’s what we’ve got to help you out:

[>> http://open.iframe.ly/api/oembed?url=…. & origin=…](http://open.iframe.ly/api/oembed?url=http://vimeo.com/62092214&origin=)

Where `url` is URL-encoded and `origin` should contain a string with either your GitHub username or your Twitter @handle (which is perhaps the same for most of you).  

More request parameters are available too. [See docs](https://iframely.com/docs) (except `&iframe=1` parameter, which activates hosted iFrames).

The embed codes will be responsive whenever possible, will cover all our 1600+ domains, and will provide [summary cards](https://iframely.com/docs/widgets) for  articles and general links that do not have native embeds. Plus CORS and JSONP so that you can call API with your JavaScript code. 

## For your site

If you publish Twitter Cards or Open Graph, Iframely can convert those into [oEmbed](http://oembed.com) so that you can easily publish your embeds to developers who auto-discover  in oEmbed format.

For it, you just add the following markup into `<head>` section of your page:

		<link rel="alternate" href="http://open.iframe.ly/api/oembed?url=...&origin=..." 
				type="application/json+oembed" />
		<link rel="alternate" href="http://open.iframe.ly/api/oembed?url=...&origin=...&format=xml"
				type="application/xml+oembed"/>

Where `url` is URL-encoded and `origin` should contain a string with either your GitHub username or your Twitter @handle (which is perhaps the same for most of you).

Twitter players, photos and Open Graph videos work best. [Debug your URLs](http://iframely.com/domain) and [whitelist your domain](https://iframely.com/qa/request) for proper coverage. Otherwise, Iframely will generate a [summary card](https://iframely.com/docs/widgets). 

Contact us if you need a custom parser for your embeds.


## Terms

* This open API endpoint is powered by [Iframely](https://iframely.com) cloud and have the same uptime guarantee. 
* In your open-source project, make the endpoint address a config variable so that your users can re-configure it to point to any of oEmbed gateways of their choosing when they start using it.
* Mention the fact that they need to configure oEmbed API endpoint in your README file or where appropriate. 
* Be nice. We reserve the right to rate-limit or block IP addresses. No rate-limit is there by default (we presume innocence). So, 
* Make sure we can contact you in case of an issue. Based on your `origin` value, if your GitHub profile doesn’t list an email address, please, consider following [Iframely on Twitter](https://twitter.com/iframely) so we can send a direct message. 
* Other standard Iframely [terms](https://iframely.com/terms) apply.


## Implementations:

Fork [this document on GitHub](https://github.com/itteco/oembed-api) and pull-request with the link to your open-source project to list it here.


* [CKEditor](https://github.com/ckeditor/ckeditor-dev) text editor 
* [Medium Insert](https://github.com/orthes/medium-editor-insert-plugin) plugin for [MediumEditor](https://github.com/daviferreira/medium-editor)
* [hypeEmbed](https://github.com/hypeJunction/hypeEmbed) plugin for Elgg community software
* Iframely for [WordPress](https://wordpress.org/plugins/iframely)