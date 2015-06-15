## KilatStorage S3 PHP Class

- - - -

About | Description
------------ | -------------
Stable tag | 0.1.3
License | GPLv2 or later
License URI | http://www.gnu.org/licenses/gpl-2.0.html

### Description

This class is a standalone S3 REST implementation for PHP 5.2.x (using CURL), that supports large file uploads and doesn’t require PEAR.

### Notes

* Not tested yet on HTTPS endpoint.

### Usage

```php
$s3 = new S3($KilatStorageAccessKey, $KilatStorageSecretKey);
```


#### Object Operations

Put an object from a file:

```php
S3::putObject(S3::inputFile($file, false), $bucket_name, $upload_name, S3::ACL_PUBLIC_READ)
```

Copy an object:

```php
S3::copyObject($src_bucket_name, $src_uri, $target_bucket_name, $target_uri)
```


Delete an object:

```php
S3::deleteObject($bucket_name, $upload_name)
```


#### Bucket Operations

Get a list of buckets:

```php
S3::listBuckets()
```

Create a bucket:

```php
S3::putBucket($bucket_name)
```

Get the contents of a bucket:

```php
S3::getBucket($bucket_name)
```

Delete an empty bucket:

```php
S3::deleteBucket($bucket_name)
```