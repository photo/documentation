Photo Imports
====================

## What sites are supported?
We currently provide importers for Facebook, Instagram, Flickr (Pro only), and Amazon S3 (Pro only). More importers are coming soon.

## How can I import my photos?
You can import your photos through the Upload photos page when you're logged into Trovebox. At the bottom of the Upload photos page are links to import photos from Flickr, Facebook, or Instagram. Select the site(s) you'd like to import from and follow the instructions.

## What information do you import?
The information we import depends on where we're importing from. We try to extract as much info as possible in addition to the images themselves. Unfortunately we don't import comments, favorites, or likes due to ownership issues.

From Flickr we import: images, titles, descriptions, camera info, location, privacy, sets (as albums), tags, license info

From Facebook we import: photos uploaded, cover photos (optional), profile photos (optional), photos you're tagged in (optional), titles, privacy, location, albums, user tags (as tags)

From Instagram we import: images, titles, hashtags (as tags), and location

From S3 we import your photos along with as much as we can based on what's already in your photo's metadata.

## How do your importers work?
Our importer fetches the information from the site requested and download it to our servers, then uploads the photos and metadata to your Trovebox site. Nothing gets downloaded to your computer.

## I requested an import, so why do I see empty albums and no new photos?
Our importer fetches your albums first, then places your import request in a line behind everyone else who has requested an import. Because of this you may see empty albums until your import starts.

## What happens if I run an importer again?
The importer ignores any duplicate photos and will fetch only any new photos you may have uploaded.

## Can I import my photos from an existing S3 bucket?
Yes. Visit [our S3 import page](https://trovebox.com/for/s3/import) to get started. This is a Pro account feature.

## Can I keep uploading to another photo site and still view that photo in Trovebox? What about uploading to Trovebox and viewing that photo elsewhere without uploading it in two places?
We don't offer a way to do this directly through Trovebox, but you can use sites like <a href="http://ifttt.com">ifttt</a> or <a href="http://pi.pe">Pixelpipe</a> that will automatically upload a picture to Trovebox when you upload a picture somewhere else (or vice versa). We've created two ifttt recipes for [Flickr to Trovebox](https://ifttt.com/recipes/16965) and [Instagram to Trovebox](https://ifttt.com/recipes/16959).

## You don't have an importer for my site or photo manager. Can I request it?
Yes. The more requests we get for an importer the faster it'll get built. Email [support@trovebox.com](support@trovebox.com) to request an importer for your photo site.
