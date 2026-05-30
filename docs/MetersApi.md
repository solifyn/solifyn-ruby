# Solifyn::MetersApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**events_ingest**](MetersApi.md#events_ingest) | **POST** /v1/meters/ingest | Ingest Events |
| [**meters_create**](MetersApi.md#meters_create) | **POST** /v1/meters | Create Meter |
| [**meters_get**](MetersApi.md#meters_get) | **GET** /v1/meters/{id} | Retrieve Meter |
| [**meters_get_events**](MetersApi.md#meters_get_events) | **GET** /v1/meters/{id}/events | List Meter Events |
| [**meters_get_quantities**](MetersApi.md#meters_get_quantities) | **GET** /v1/meters/{id}/quantities | Get Meter Quantities |
| [**meters_list**](MetersApi.md#meters_list) | **GET** /v1/meters | List Meters |
| [**meters_update**](MetersApi.md#meters_update) | **PATCH** /v1/meters/{id} | Update Meter |


## events_ingest

> <MeterIngestResponseDto> events_ingest(meter_ingest_request_dto)

Ingest Events

Ingest usage events for meters.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::MetersApi.new
meter_ingest_request_dto = Solifyn::MeterIngestRequestDto.new({events: [Solifyn::MeterIngestEventDto.new({event_id: 'evt_9Y3kP4qR7tU1vW2xZ5aB6c', customer_id: 'cus_8n7m6l5k4j3h2g1f0e9d8c', event_name: 'api.request'})]}) # MeterIngestRequestDto | 

begin
  # Ingest Events
  result = api_instance.events_ingest(meter_ingest_request_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->events_ingest: #{e}"
end
```

#### Using the events_ingest_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MeterIngestResponseDto>, Integer, Hash)> events_ingest_with_http_info(meter_ingest_request_dto)

```ruby
begin
  # Ingest Events
  data, status_code, headers = api_instance.events_ingest_with_http_info(meter_ingest_request_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MeterIngestResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->events_ingest_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **meter_ingest_request_dto** | [**MeterIngestRequestDto**](MeterIngestRequestDto.md) |  |  |

### Return type

[**MeterIngestResponseDto**](MeterIngestResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## meters_create

> <MeterResponseDto> meters_create(create_meter_dto)

Create Meter

Create a new usage meter for event-based billing and usage tracking.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::MetersApi.new
create_meter_dto = Solifyn::CreateMeterDto.new({name: 'API Request Count', event_name: 'api.request', aggregation_type: 'COUNT'}) # CreateMeterDto | 

begin
  # Create Meter
  result = api_instance.meters_create(create_meter_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->meters_create: #{e}"
end
```

#### Using the meters_create_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MeterResponseDto>, Integer, Hash)> meters_create_with_http_info(create_meter_dto)

```ruby
begin
  # Create Meter
  data, status_code, headers = api_instance.meters_create_with_http_info(create_meter_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MeterResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->meters_create_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **create_meter_dto** | [**CreateMeterDto**](CreateMeterDto.md) |  |  |

### Return type

[**MeterResponseDto**](MeterResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## meters_get

> <MeterDetailResponseDto> meters_get(id, start_date, end_date)

Retrieve Meter

Retrieve a meter and its most recent usage events.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::MetersApi.new
id = 'mtr_8Z1aB2cD3eF4gH5iJ6kL7m' # String | The unique meter ID.
start_date = 'start_date_example' # String | 
end_date = 'end_date_example' # String | 

begin
  # Retrieve Meter
  result = api_instance.meters_get(id, start_date, end_date)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->meters_get: #{e}"
end
```

#### Using the meters_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MeterDetailResponseDto>, Integer, Hash)> meters_get_with_http_info(id, start_date, end_date)

```ruby
begin
  # Retrieve Meter
  data, status_code, headers = api_instance.meters_get_with_http_info(id, start_date, end_date)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MeterDetailResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->meters_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique meter ID. |  |
| **start_date** | **String** |  |  |
| **end_date** | **String** |  |  |

### Return type

[**MeterDetailResponseDto**](MeterDetailResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## meters_get_events

> <MeterEventsResponseDto> meters_get_events(id, opts)

List Meter Events

List recent usage events recorded for a meter.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::MetersApi.new
id = 'mtr_8Z1aB2cD3eF4gH5iJ6kL7m' # String | The unique meter ID.
opts = {
  limit: 8.14 # Float | Maximum number of usage events to return.
}

begin
  # List Meter Events
  result = api_instance.meters_get_events(id, opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->meters_get_events: #{e}"
end
```

#### Using the meters_get_events_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MeterEventsResponseDto>, Integer, Hash)> meters_get_events_with_http_info(id, opts)

```ruby
begin
  # List Meter Events
  data, status_code, headers = api_instance.meters_get_events_with_http_info(id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MeterEventsResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->meters_get_events_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique meter ID. |  |
| **limit** | **Float** | Maximum number of usage events to return. | [optional][default to 100] |

### Return type

[**MeterEventsResponseDto**](MeterEventsResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## meters_get_quantities

> <MeterQuantitiesResponseDto> meters_get_quantities(id, opts)

Get Meter Quantities

Get aggregated usage quantities for a meter within an optional date range.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::MetersApi.new
id = 'mtr_8Z1aB2cD3eF4gH5iJ6kL7m' # String | The unique meter ID.
opts = {
  start_date: 'start_date_example', # String | Inclusive start date in ISO 8601 format.
  end_date: 'end_date_example' # String | Inclusive end date in ISO 8601 format.
}

begin
  # Get Meter Quantities
  result = api_instance.meters_get_quantities(id, opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->meters_get_quantities: #{e}"
end
```

#### Using the meters_get_quantities_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MeterQuantitiesResponseDto>, Integer, Hash)> meters_get_quantities_with_http_info(id, opts)

```ruby
begin
  # Get Meter Quantities
  data, status_code, headers = api_instance.meters_get_quantities_with_http_info(id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MeterQuantitiesResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->meters_get_quantities_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique meter ID. |  |
| **start_date** | **String** | Inclusive start date in ISO 8601 format. | [optional] |
| **end_date** | **String** | Inclusive end date in ISO 8601 format. | [optional] |

### Return type

[**MeterQuantitiesResponseDto**](MeterQuantitiesResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## meters_list

> <Array<MeterResponseDto>> meters_list(opts)

List Meters

List meters belonging to your active business. You can filter by archived status.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::MetersApi.new
opts = {
  status: 'active' # String | Filter by meter status.
}

begin
  # List Meters
  result = api_instance.meters_list(opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->meters_list: #{e}"
end
```

#### Using the meters_list_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Array<MeterResponseDto>>, Integer, Hash)> meters_list_with_http_info(opts)

```ruby
begin
  # List Meters
  data, status_code, headers = api_instance.meters_list_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Array<MeterResponseDto>>
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->meters_list_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** | Filter by meter status. | [optional] |

### Return type

[**Array&lt;MeterResponseDto&gt;**](MeterResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## meters_update

> <MeterResponseDto> meters_update(id, update_meter_dto)

Update Meter

Update an existing meter definition.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::MetersApi.new
id = 'mtr_8Z1aB2cD3eF4gH5iJ6kL7m' # String | The unique meter ID.
update_meter_dto = Solifyn::UpdateMeterDto.new # UpdateMeterDto | 

begin
  # Update Meter
  result = api_instance.meters_update(id, update_meter_dto)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->meters_update: #{e}"
end
```

#### Using the meters_update_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<MeterResponseDto>, Integer, Hash)> meters_update_with_http_info(id, update_meter_dto)

```ruby
begin
  # Update Meter
  data, status_code, headers = api_instance.meters_update_with_http_info(id, update_meter_dto)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <MeterResponseDto>
rescue Solifyn::ApiError => e
  puts "Error when calling MetersApi->meters_update_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique meter ID. |  |
| **update_meter_dto** | [**UpdateMeterDto**](UpdateMeterDto.md) |  |  |

### Return type

[**MeterResponseDto**](MeterResponseDto.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

