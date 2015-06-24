s3cmd-signed-url
================

Create temporary signed urls for private S3/Riak CS buckets using the s3cmd.

#### Dependencies

The `s3cmd-signed-url` depends on [s3cmd](http://s3tools.org/s3cmd).

#### Usage

    s3cmd-signed-url -b bucket -o object_uri [-a access_key] [-s seconds] [-v verb] [-c scheme]

#### Options

    -b bucket_name: bucket name (example: my-bucket)
    -o object_uri: URI part of object in S3 bucket (example: somefolder/somefile.ext)
	-v http_verb: HTTP verb to access a object in S3 bucket (default ${HTTP_VERB})
	-c scheme: Scheme of url (default ${S3_SCHEME})
    -a access_key: S3 Access Key (default: Access key in ${HOME}/.s3cfg: ${S3_ACCESS_KEY})
    -s seconds: how long the signed url will be valid (default 3600)
    -h: see this usage information