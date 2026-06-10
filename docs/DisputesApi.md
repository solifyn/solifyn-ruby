# Solifyn::DisputesApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**disputes_generate_report**](DisputesApi.md#disputes_generate_report) | **GET** /v1/transactions/disputes/report | Generate Dispute CSV Report |
| [**disputes_get**](DisputesApi.md#disputes_get) | **GET** /v1/transactions/disputes/{id} | Retrieve Dispute |
| [**disputes_list**](DisputesApi.md#disputes_list) | **GET** /v1/transactions/disputes | List Disputes |
| [**disputes_submit_evidence**](DisputesApi.md#disputes_submit_evidence) | **POST** /v1/transactions/disputes/{id}/submit | Submit Dispute Evidence |
| [**disputes_update_evidence**](DisputesApi.md#disputes_update_evidence) | **PATCH** /v1/transactions/disputes/{id}/evidence | Update Dispute Evidence |
| [**disputes_upload_evidence_file**](DisputesApi.md#disputes_upload_evidence_file) | **POST** /v1/transactions/disputes/upload | Upload Evidence File |


## disputes_generate_report

> disputes_generate_report(opts)

Generate Dispute CSV Report

Generates a downloadable CSV report of disputes matching the filters.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DisputesApi.new
opts = {
  created_at_gte: 'created_at_gte_example', # String | Filter disputes created after this ISO date-time string
  created_at_lte: 'created_at_lte_example', # String | Filter disputes created before this ISO date-time string
  status: 'status_example' # String | Filter disputes by status
}

begin
  # Generate Dispute CSV Report
  api_instance.disputes_generate_report(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DisputesApi->disputes_generate_report: #{e}"
end
```

#### Using the disputes_generate_report_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> disputes_generate_report_with_http_info(opts)

```ruby
begin
  # Generate Dispute CSV Report
  data, status_code, headers = api_instance.disputes_generate_report_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DisputesApi->disputes_generate_report_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **created_at_gte** | **String** | Filter disputes created after this ISO date-time string | [optional] |
| **created_at_lte** | **String** | Filter disputes created before this ISO date-time string | [optional] |
| **status** | **String** | Filter disputes by status | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined


## disputes_get

> <Dispute> disputes_get(id)

Retrieve Dispute

Retrieve details of a specific dispute by ID.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DisputesApi.new
id = 'dsp_123' # String | The dispute ID

begin
  # Retrieve Dispute
  result = api_instance.disputes_get(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DisputesApi->disputes_get: #{e}"
end
```

#### Using the disputes_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Dispute>, Integer, Hash)> disputes_get_with_http_info(id)

```ruby
begin
  # Retrieve Dispute
  data, status_code, headers = api_instance.disputes_get_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Dispute>
rescue Solifyn::ApiError => e
  puts "Error when calling DisputesApi->disputes_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The dispute ID |  |

### Return type

[**Dispute**](Dispute.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## disputes_list

> <DisputeList> disputes_list(opts)

List Disputes

Retrieve disputes associated with the active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DisputesApi.new
opts = {
  page: '1', # String | Page number for pagination
  limit: '10', # String | Page size limit for pagination
  status: 'status_example', # String | Filter disputes by status
  type: 'type_example' # String | Filter by type: dispute or alert
}

begin
  # List Disputes
  result = api_instance.disputes_list(opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DisputesApi->disputes_list: #{e}"
end
```

#### Using the disputes_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DisputeList>, Integer, Hash)> disputes_list_with_http_info(opts)

```ruby
begin
  # List Disputes
  data, status_code, headers = api_instance.disputes_list_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DisputeList>
rescue Solifyn::ApiError => e
  puts "Error when calling DisputesApi->disputes_list_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **page** | **String** | Page number for pagination | [optional] |
| **limit** | **String** | Page size limit for pagination | [optional] |
| **status** | **String** | Filter disputes by status | [optional] |
| **type** | **String** | Filter by type: dispute or alert | [optional] |

### Return type

[**DisputeList**](DisputeList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## disputes_submit_evidence

> <Dispute> disputes_submit_evidence(id)

Submit Dispute Evidence

Finalize and submit the uploaded evidence for review.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DisputesApi.new
id = 'dsp_123' # String | The dispute ID

begin
  # Submit Dispute Evidence
  result = api_instance.disputes_submit_evidence(id)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DisputesApi->disputes_submit_evidence: #{e}"
end
```

#### Using the disputes_submit_evidence_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Dispute>, Integer, Hash)> disputes_submit_evidence_with_http_info(id)

```ruby
begin
  # Submit Dispute Evidence
  data, status_code, headers = api_instance.disputes_submit_evidence_with_http_info(id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Dispute>
rescue Solifyn::ApiError => e
  puts "Error when calling DisputesApi->disputes_submit_evidence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The dispute ID |  |

### Return type

[**Dispute**](Dispute.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## disputes_update_evidence

> <Dispute> disputes_update_evidence(id, dispute_evidence_update)

Update Dispute Evidence

Upload and update evidence attachments for a dispute.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DisputesApi.new
id = 'dsp_123' # String | The dispute ID
dispute_evidence_update = Solifyn::DisputeEvidenceUpdate.new # DisputeEvidenceUpdate | 

begin
  # Update Dispute Evidence
  result = api_instance.disputes_update_evidence(id, dispute_evidence_update)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DisputesApi->disputes_update_evidence: #{e}"
end
```

#### Using the disputes_update_evidence_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Dispute>, Integer, Hash)> disputes_update_evidence_with_http_info(id, dispute_evidence_update)

```ruby
begin
  # Update Dispute Evidence
  data, status_code, headers = api_instance.disputes_update_evidence_with_http_info(id, dispute_evidence_update)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Dispute>
rescue Solifyn::ApiError => e
  puts "Error when calling DisputesApi->disputes_update_evidence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The dispute ID |  |
| **dispute_evidence_update** | [**DisputeEvidenceUpdate**](DisputeEvidenceUpdate.md) |  |  |

### Return type

[**Dispute**](Dispute.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## disputes_upload_evidence_file

> <DisputeFileUpload> disputes_upload_evidence_file(file)

Upload Evidence File

Upload a support file (image, PDF, video) to use as dispute evidence.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DisputesApi.new
file = File.new('/path/to/some/file') # File | The evidence file to upload (Max 25MB: JPEG, PNG, GIF, WEBP, PDF, MP4, WEBM, QuickTime)

begin
  # Upload Evidence File
  result = api_instance.disputes_upload_evidence_file(file)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling DisputesApi->disputes_upload_evidence_file: #{e}"
end
```

#### Using the disputes_upload_evidence_file_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DisputeFileUpload>, Integer, Hash)> disputes_upload_evidence_file_with_http_info(file)

```ruby
begin
  # Upload Evidence File
  data, status_code, headers = api_instance.disputes_upload_evidence_file_with_http_info(file)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DisputeFileUpload>
rescue Solifyn::ApiError => e
  puts "Error when calling DisputesApi->disputes_upload_evidence_file_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **file** | **File** | The evidence file to upload (Max 25MB: JPEG, PNG, GIF, WEBP, PDF, MP4, WEBM, QuickTime) |  |

### Return type

[**DisputeFileUpload**](DisputeFileUpload.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

