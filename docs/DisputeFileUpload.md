# Solifyn::DisputeFileUpload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Uploaded file ID |  |
| **filename** | **String** | Name of the file |  |
| **upload_url** | **String** | S3 presigned upload URL | [optional] |
| **upload_headers** | **Object** | HTTP headers required for the S3 upload request | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::DisputeFileUpload.new(
  id: file_123,
  filename: evidence.png,
  upload_url: https://whop-s3-upload-url...,
  upload_headers: null
)
```

