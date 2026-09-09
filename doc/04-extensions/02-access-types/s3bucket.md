# S3Bucket — Blob hosted in an S3 compatible bucket

## Synopsis

```text
type: S3Bucket[/VERSION]
[ATTRIBUTES]
```

Type name `s3Bucket` is supported as an alias.

> **Note:** `S3Bucket` is a different type than the legacy [`S3`](s3.md) access
> type. It is not an alias of `S3`.

## Description

Access to a single object stored in an S3 API compatible bucket.

The same specification format is also used as the `S3Bucket` input type, which
stores the object as a [local blob](localblob.md) in the component version.

## Supported Media Types

The provided media type is taken from the specification attribute `mediaType`.

## Specification Version

The following versions are supported

### v1

Attributes:

- **`bucketName`** *string*

  The name of the bucket containing the object

- **`objectKey`** *string*

  The key of the desired object

- **`region`** (optional) *string*

  region identifier of the used store

- **`mediaType`** (optional) *string*

  The media type of the blob used to store the resource. It may add
  format information like `+tar` or `+gzip`.

- **`version`** (optional) *string*

  The object version (`versionId`) to read. If it is not set, the latest
  version is read.

- **`endpoint`** (optional) *string*

  The base endpoint of an S3 compatible store. If it is not set, AWS S3 is used.

- **`usePathStyle`** (optional) *bool*

  The usePathStyle describes whether the bucket is put in the path instead of
  in the host.
