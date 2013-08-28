Pro Accounts
===========================

## What do I get with a Trovebox Pro account?
With a pro account, you get:

* Unlimited photo uploads (Compare to 100 photos/month for free users)
* Import your photos from Flickr, Facebook, and Instagram. Picasa and Smugmug are coming soon.
* Switch where you store your photos as many times as you wish
* Give multiple users access on your account without giving them your password
* Top level domain support at yourdomain.com

<a href="https://trovebox.com/plans">Check out our plans chart</a> for the full breakdown.

## How much does a Pro account cost?
A Pro account costs $29.99 a year.

## How do I upgrade from a free account to a Pro account?
Visit <a href="https://trovebox.com/upgrade">our upgrade page</a>, enter your credit card info, and enjoy your Pro account!

## Can I select a Pro plan when I sign up for Trovebox?
Yes. When you sign up, select the Pro plan, and you'll be prompted for your credit card info.

## Can I pay via PayPal? Google Wallet? Some other way?
Not yet. If you have any trouble getting your Pro account with a credit card contact us at [support@trovebox.com](mailto:support@trovebox.com) and we can figure out a way.

## Is there a monthly Pro plan?
Not directly through the website, but you can purchase a monthly plan for $2.99/month straight through the iPhone app. Monthly plan support for the Android app is planned.

## Is unlimited really unlimited? What's the catch?
We don't limit uploads for Pro users, but you may face limits from your storage provider. If we're your storage provider then everything is unlimited. 

## Do you store users' credit card info?
No, we don't. Your credit card info doesn't go through our servers at all, instead traveling securely from your server to our payment processor's.

## Do I have to renew manually every year?
Nope. We'll alert you when your Pro account is going to renew.

## What happens if my Pro subscription ends?
Don't panic! Nothing has been deleted. You resume using a free account, though you're now subject to the free account limitations. You can still access all your photos, free or Pro.

## What can collaborators do with my account?
Collaborators can add photos, edit photos, delete photos--just about anything you can do except delete your account. When you add them as a collaborator they can log in with that email via Mozilla Persona. Soon they'll be able to 
log in via the regular Trovebox login.

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

## My needs go far beyond what a Pro account provides. Can I get even more?
We're working on a <a href="https://trovebox.com/organizations">plan for organizations</a>. Email us at <a href="mailto:support@trovebox.com">support@trovebox.com</a> if you're interested.
