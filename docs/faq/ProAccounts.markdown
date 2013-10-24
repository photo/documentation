Pro Accounts
===========================

## I've heard that Pro accounts are no longer being offered. What does that mean for me?
As of 25 October 2013, new Unlimited Pro accounts are no longer available for purchase. Current Pro accounts will continue to be honored and renewed at the same $29.99 per year rate.

## What did Trovebox Pro account holders receive?
Pro account holders receive:

* Unlimited photo uploads (Compare to 100 photos/month for free users)
* Import your photos from Flickr, Facebook, and Instagram. Picasa and Smugmug are coming soon.
* Switch where you store your photos as many times as you wish
* Give multiple users access on your account without giving them your password
* Top level domain support at yourdomain.com

These features are now available with our current plans.

## Do you store users' credit card info?
No, we don't. Your credit card info doesn't go through our servers at all, instead traveling securely from your server to our payment processor's.

## Do I have to renew manually every year?
Nope. We'll alert you when your Pro account is going to renew.

## What happens if my Pro subscription ends?
Don't panic! Nothing has been deleted. You resume using a free account, though you're now subject to the free account limitations. You can still access all your photos. You can also choose to upgrade to one of your new plans.

## What can collaborators do with my account?
Collaborators can add photos, edit photos, delete photos--just about anything you can do except delete your account. When you add a collaborator, we send them an email prompting them to set a password.

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
