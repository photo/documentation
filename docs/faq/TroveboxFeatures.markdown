Trovebox Features
==============

## What is white-labeling?

White-labeling is a feature that lets you design your Trovebox site with your organization’s logo and colors. Your visitors will automatically recognize your Trovebox site as yours.

## How does white-labeling at Trovebox work?

Email us at support@trovebox.com with what you’d like modified on your Trovebox site. Currently we can modify Soon we’ll offer a way for you to do this yourself.

## What is the Trovebox Consultancy Service?

The consultancy service connects you to a Trovebox developer who can help you integrate Trovebox with your company’s website. 

## What’s the Getting Started web conference?

When you sign up for the Platinum plan, one of our Trovebox team members will This feature is available for Platinum members.

## How do I upload video?

Video is coming very soon, but once it's here you can upload video the same way you upload photos.

## How do I add a top level domain?
Adding a top level domain to your Trovebox site is currently all manual on our end, so there are two steps to take. First, email <a href="mailto:support@trovebox.com">support@trovebox.com</a> with the domain or subdomain you'd like to add to your Trovebox site.

After we've replied and confirmed that we've set up your domain, you'll need to create a CNAME record for your domain. This is a type of DNS resource record, so consult your domain registrar's documentation on where to set it. DNS settings are a good place to start. Enter the following where prompted:

* Name: your subdomain
* Type:	CNAME
* Data (or Alias):	yourusername.trovebox.com.

It'll take up to 24 hours for your changes to take effect.

## How do I add Twitter cards for my domain?
Twitter cards are added per domain over at Twitter. You can <a href="https://dev.twitter.com/docs/cards">apply for them separately</a> for your own domain there.

## Can I use a custom domain for my Trovebox thumbnails?
Yes. If you're already using a subdomain on your Trovebox site, you should use a different one for your images so one subdomain doesn't map to two places.

The easiest way to use a domain for your thumbnails is to store your photos in an Amazon S3 bucket named after your subdomain--that is, your.subdomain.com. Then add a CNAME record pointing your.subdomain.com to your.subdomain.com.s3.amazonaws.com. Once you've done this email us at <a href="mailto:support@trovebox.com">support@trovebox.com</a> and we can update the record on our side.
