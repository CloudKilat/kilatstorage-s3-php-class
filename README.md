## KilatStorage S3 PHP Class

- - - -

About | Description
------------ | -------------
Stable tag | 0.1.2
License | GPLv2 or later
License URI | http://www.gnu.org/licenses/gpl-2.0.html

### Description

This class is a standalone S3 REST implementation for PHP 5.2.x (using CURL), that supports large file uploads and doesn’t require PEAR.

### Notes

* Some methods are not implemented yet, such as copy object.
* Not tested yet on HTTPS endpoint.

### Usage

```php
$s3 = new S3($KilatStorageAccessKey, $KilatStorageSecretKey);

#### Object Operations

Put an object from a file:

```php
S3::putObjectFile($file, $bucket, $uri, $acl = self::ACL_PRIVATE, $metaHeaders = array(), $contentType = null)
```

Delete an object:

```php
S3::deleteObject($bucketName, $uploadName)
```


#### Bucket Operations

Get a list of buckets:

```php
S3::listBuckets()
```

Create a bucket:

```php
S3::putBucket($bucketName)
```

Get the contents of a bucket:

```php
S3::getBucket($bucketName)
```

Delete an empty bucket:

```php
S3::deleteBucket($bucketName)
```