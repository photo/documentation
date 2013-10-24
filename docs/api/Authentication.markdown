Authentication using OAuth 1.0a
=======================

### Using OAuth (1.0a)

A full introduction to OAuth is beyond the scope of the OpenPhoto documentation.
In all reality you probably don't need to understand all the ins and outs of OAuth; just grab one of our libraries and start building.

* <a href="https://github.com/photo/openphoto-php">Our PHP language binding</a>
* <a href="https://github.com/photo/openphoto-ruby">Our Ruby language binding</a>
* <a href="https://github.com/photo/openphoto-python">Our Python language binding</a>
* <a href="https://github.com/photo/openphoto-java">Our Java language binding</a>
* <a href="https://github.com/photo/openphoto-javascript">Our Javascript language binding</a>
* <a href="https://github.com/photo/openphoto-objective-c">Our Objective-C language binding</a>
* More coming soon, <a href="mailto:openphoto@googlegroups.com">contact us</a> if you'd like to write bindings in an unlisted language.

### Obtaining a consumer key and secret

Since OpenPhoto is distributed the flow to obtain a consumer key and secret differs slightly from typical OAuth applications.
Typically you would sign up for an application ID and be given a key and secret to be used with your app.
OpenPhoto differs because the host you'll be sending requests to is arbitrary and there's no central application repository.

The easiest way to create a consumer key and secret is to browse to browse to your OpenPhoto site and go to `/v1/oauth/flow`. Follow the prompts until you get a success message. Then go to `/manage/apps` and you should see the following parameters:

* Consumer Key
* Consumer Secret
* OAuth Token
* OAuth Secret

### Resources on the web

If you're interested in learning more about OAuth then the following links are a great place to start.

* <a href="http://oauth.net/documentation/getting-started/">http://oauth.net/documentation/getting-started/</a>
* <a href="http://hueniverse.com/oauth/guide/intro/">http://hueniverse.com/oauth/guide/intro/</a>
* <a href="http://www.slideshare.net/eran/introduction-to-oauth-presentation">http://www.slideshare.net/eran/introduction-to-oauth-presentation</a>
