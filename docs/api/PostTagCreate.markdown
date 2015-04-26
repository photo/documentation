Create Tag
=======================


----------------------------------------

1. [Purpose][purpose]
1. [Endpoint][endpoint]
1. [Parameters][parameters]
1. [Examples][examples]
  * [Command line][example-cli]
  * [PHP][example-php]
1. [Response][response]
  * [Sample][sample]

----------------------------------------

<a name="purpose"></a>
### Purpose of the Create Tag API

This API is used internally to create a tag.
External applications should use the [Photo Update API](http://theopenphotoproject.org/documentation/api/PostPhotoUpdate) to create tags.

----------------------------------------

<a name="endpoint"></a>
### Endpoint

_Authentication: required_

    POST /tag/create.json

<a name="parameters"></a>
### Parameters

1.  tag (required), The name of the tag to create
1.  count (optional), Number of photos which contain this tag

----------------------------------------

<a name="examples"></a>
### Examples

<a name="example-cli"></a>
#### Command Line (using [openphoto-php][openphoto-php])

    ./openphoto -p -X POST -h current.openphoto.me -e /tag/create.json -F 'tag=sunnyvale' -F 'count=10'

<a name="example-php"></a>
#### PHP (using [openphoto-php][openphoto-php])

    $client = new OpenPhotoOAuth($host, $consumerKey, $consumerSecret, $oauthToken, $oauthTokenSecret);
    $response = $client->post("/tag/create.json", array('tag' => 'sunnyvale', 'count' => 10));

----------------------------------------

<a name="response"></a>
### Response

The response is in a standard [response envelope](http://theopenphotoproject.org/documentation/api/Envelope).

* _message_, A string describing the result. Don't use this for anything but reading.
* _code_, _201_ on success
* _result_, TRUE if the tag was successfully created

<a name="sample"></a>
#### Sample

    {
      "message":"",
      "code":201,
      "result":TRUE
    }


[Tag]: http://theopenphotoproject.org/documentation/schemas/Tag
[purpose]: #purpose
[endpoint]: #endpoint
[parameters]: #parameters
[examples]: #examples
[example-cli]: #example-cli
[example-php]: #example-php
[response]: #response
[sample]: #sample
[openphoto-php]: https://github.com/photo/openphoto-php

