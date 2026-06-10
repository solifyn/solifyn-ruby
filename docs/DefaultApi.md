# Solifyn::DefaultApi

All URIs are relative to *https://api.solifyn.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**dispute_created_post**](DefaultApi.md#dispute_created_post) | **POST** /dispute.created | Dispute Created |
| [**dispute_lost_post**](DefaultApi.md#dispute_lost_post) | **POST** /dispute.lost | Dispute Lost |
| [**dispute_won_post**](DefaultApi.md#dispute_won_post) | **POST** /dispute.won | Dispute Won |
| [**entitlement_grant_created_post**](DefaultApi.md#entitlement_grant_created_post) | **POST** /entitlement_grant.created | Entitlement Grant Created |
| [**entitlement_grant_delivered_post**](DefaultApi.md#entitlement_grant_delivered_post) | **POST** /entitlement_grant.delivered | Entitlement Grant Delivered |
| [**entitlement_grant_failed_post**](DefaultApi.md#entitlement_grant_failed_post) | **POST** /entitlement_grant.failed | Entitlement Grant Failed |
| [**entitlement_grant_revoked_post**](DefaultApi.md#entitlement_grant_revoked_post) | **POST** /entitlement_grant.revoked | Entitlement Grant Revoked |
| [**license_created_post**](DefaultApi.md#license_created_post) | **POST** /license.created | License Created |
| [**license_revoked_post**](DefaultApi.md#license_revoked_post) | **POST** /license.revoked | License Revoked |
| [**payment_created_post**](DefaultApi.md#payment_created_post) | **POST** /payment.created | Payment Created |
| [**payment_failed_post**](DefaultApi.md#payment_failed_post) | **POST** /payment.failed | Payment Failed |
| [**payment_succeeded_post**](DefaultApi.md#payment_succeeded_post) | **POST** /payment.succeeded | Payment Succeeded |
| [**refund_failed_post**](DefaultApi.md#refund_failed_post) | **POST** /refund.failed | Refund Failed |
| [**refund_succeeded_post**](DefaultApi.md#refund_succeeded_post) | **POST** /refund.succeeded | Refund Succeeded |
| [**subscription_created_post**](DefaultApi.md#subscription_created_post) | **POST** /subscription.created | Subscription Created |
| [**subscription_deactivated_post**](DefaultApi.md#subscription_deactivated_post) | **POST** /subscription.deactivated | Subscription Deactivated |
| [**subscription_updated_post**](DefaultApi.md#subscription_updated_post) | **POST** /subscription.updated | Subscription Updated |


## dispute_created_post

> dispute_created_post(opts)

Dispute Created

Occurs when a payment charge is disputed by the customer (chargeback initiated).

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_dispute_payload:  # WebhookDisputePayload | 
}

begin
  # Dispute Created
  api_instance.dispute_created_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->dispute_created_post: #{e}"
end
```

#### Using the dispute_created_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> dispute_created_post_with_http_info(opts)

```ruby
begin
  # Dispute Created
  data, status_code, headers = api_instance.dispute_created_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->dispute_created_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_dispute_payload** | [**WebhookDisputePayload**](WebhookDisputePayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## dispute_lost_post

> dispute_lost_post(opts)

Dispute Lost

Occurs when a dispute challenge is lost and the funds are returned to the cardholder.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_dispute_payload:  # WebhookDisputePayload | 
}

begin
  # Dispute Lost
  api_instance.dispute_lost_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->dispute_lost_post: #{e}"
end
```

#### Using the dispute_lost_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> dispute_lost_post_with_http_info(opts)

```ruby
begin
  # Dispute Lost
  data, status_code, headers = api_instance.dispute_lost_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->dispute_lost_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_dispute_payload** | [**WebhookDisputePayload**](WebhookDisputePayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## dispute_won_post

> dispute_won_post(opts)

Dispute Won

Occurs when a dispute challenge is won by the merchant.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_dispute_payload:  # WebhookDisputePayload | 
}

begin
  # Dispute Won
  api_instance.dispute_won_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->dispute_won_post: #{e}"
end
```

#### Using the dispute_won_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> dispute_won_post_with_http_info(opts)

```ruby
begin
  # Dispute Won
  data, status_code, headers = api_instance.dispute_won_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->dispute_won_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_dispute_payload** | [**WebhookDisputePayload**](WebhookDisputePayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## entitlement_grant_created_post

> entitlement_grant_created_post(opts)

Entitlement Grant Created

Occurs when a new entitlement grant is created (e.g., at checkout completion if the product has GitHub access). The collaborator invitation is pending.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_entitlement_grant_payload:  # WebhookEntitlementGrantPayload | 
}

begin
  # Entitlement Grant Created
  api_instance.entitlement_grant_created_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->entitlement_grant_created_post: #{e}"
end
```

#### Using the entitlement_grant_created_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> entitlement_grant_created_post_with_http_info(opts)

```ruby
begin
  # Entitlement Grant Created
  data, status_code, headers = api_instance.entitlement_grant_created_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->entitlement_grant_created_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_entitlement_grant_payload** | [**WebhookEntitlementGrantPayload**](WebhookEntitlementGrantPayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## entitlement_grant_delivered_post

> entitlement_grant_delivered_post(opts)

Entitlement Grant Delivered

Occurs when the customer successfully connects their GitHub account and the collaborator invitation is successfully delivered.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_entitlement_grant_payload:  # WebhookEntitlementGrantPayload | 
}

begin
  # Entitlement Grant Delivered
  api_instance.entitlement_grant_delivered_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->entitlement_grant_delivered_post: #{e}"
end
```

#### Using the entitlement_grant_delivered_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> entitlement_grant_delivered_post_with_http_info(opts)

```ruby
begin
  # Entitlement Grant Delivered
  data, status_code, headers = api_instance.entitlement_grant_delivered_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->entitlement_grant_delivered_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_entitlement_grant_payload** | [**WebhookEntitlementGrantPayload**](WebhookEntitlementGrantPayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## entitlement_grant_failed_post

> entitlement_grant_failed_post(opts)

Entitlement Grant Failed

Occurs when invitation delivery fails (e.g., if the user GitHub account is flagged or invitation limit is reached).

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_entitlement_grant_payload:  # WebhookEntitlementGrantPayload | 
}

begin
  # Entitlement Grant Failed
  api_instance.entitlement_grant_failed_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->entitlement_grant_failed_post: #{e}"
end
```

#### Using the entitlement_grant_failed_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> entitlement_grant_failed_post_with_http_info(opts)

```ruby
begin
  # Entitlement Grant Failed
  data, status_code, headers = api_instance.entitlement_grant_failed_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->entitlement_grant_failed_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_entitlement_grant_payload** | [**WebhookEntitlementGrantPayload**](WebhookEntitlementGrantPayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## entitlement_grant_revoked_post

> entitlement_grant_revoked_post(opts)

Entitlement Grant Revoked

Occurs when the customer access is removed from the repository (manually or automatically via subscription cancel/refund).

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_entitlement_grant_payload:  # WebhookEntitlementGrantPayload | 
}

begin
  # Entitlement Grant Revoked
  api_instance.entitlement_grant_revoked_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->entitlement_grant_revoked_post: #{e}"
end
```

#### Using the entitlement_grant_revoked_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> entitlement_grant_revoked_post_with_http_info(opts)

```ruby
begin
  # Entitlement Grant Revoked
  data, status_code, headers = api_instance.entitlement_grant_revoked_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->entitlement_grant_revoked_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_entitlement_grant_payload** | [**WebhookEntitlementGrantPayload**](WebhookEntitlementGrantPayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## license_created_post

> license_created_post(opts)

License Created

Occurs when a new software license key is created or assigned to a customer purchase.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_license_payload:  # WebhookLicensePayload | 
}

begin
  # License Created
  api_instance.license_created_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->license_created_post: #{e}"
end
```

#### Using the license_created_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> license_created_post_with_http_info(opts)

```ruby
begin
  # License Created
  data, status_code, headers = api_instance.license_created_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->license_created_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_license_payload** | [**WebhookLicensePayload**](WebhookLicensePayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## license_revoked_post

> license_revoked_post(opts)

License Revoked

Occurs when a software license key is revoked (e.g., due to subscription cancellation, refund, or dispute).

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_license_payload:  # WebhookLicensePayload | 
}

begin
  # License Revoked
  api_instance.license_revoked_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->license_revoked_post: #{e}"
end
```

#### Using the license_revoked_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> license_revoked_post_with_http_info(opts)

```ruby
begin
  # License Revoked
  data, status_code, headers = api_instance.license_revoked_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->license_revoked_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_license_payload** | [**WebhookLicensePayload**](WebhookLicensePayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## payment_created_post

> payment_created_post(opts)

Payment Created

Occurs when a new payment is initiated (e.g., at checkout start or subscription creation). The payment may still be in an incomplete or pending state.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_payment_payload:  # WebhookPaymentPayload | 
}

begin
  # Payment Created
  api_instance.payment_created_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->payment_created_post: #{e}"
end
```

#### Using the payment_created_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> payment_created_post_with_http_info(opts)

```ruby
begin
  # Payment Created
  data, status_code, headers = api_instance.payment_created_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->payment_created_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_payment_payload** | [**WebhookPaymentPayload**](WebhookPaymentPayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## payment_failed_post

> payment_failed_post(opts)

Payment Failed

Occurs when a customer payment attempt fails.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  order:  # Order | 
}

begin
  # Payment Failed
  api_instance.payment_failed_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->payment_failed_post: #{e}"
end
```

#### Using the payment_failed_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> payment_failed_post_with_http_info(opts)

```ruby
begin
  # Payment Failed
  data, status_code, headers = api_instance.payment_failed_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->payment_failed_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order** | [**Order**](Order.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## payment_succeeded_post

> payment_succeeded_post(opts)

Payment Succeeded

Occurs when a customer payment is confirmed as succeeded.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  order:  # Order | 
}

begin
  # Payment Succeeded
  api_instance.payment_succeeded_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->payment_succeeded_post: #{e}"
end
```

#### Using the payment_succeeded_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> payment_succeeded_post_with_http_info(opts)

```ruby
begin
  # Payment Succeeded
  data, status_code, headers = api_instance.payment_succeeded_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->payment_succeeded_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **order** | [**Order**](Order.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## refund_failed_post

> refund_failed_post(opts)

Refund Failed

Occurs when a payment refund fails.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_refund_payload:  # WebhookRefundPayload | 
}

begin
  # Refund Failed
  api_instance.refund_failed_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->refund_failed_post: #{e}"
end
```

#### Using the refund_failed_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> refund_failed_post_with_http_info(opts)

```ruby
begin
  # Refund Failed
  data, status_code, headers = api_instance.refund_failed_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->refund_failed_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_refund_payload** | [**WebhookRefundPayload**](WebhookRefundPayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## refund_succeeded_post

> refund_succeeded_post(opts)

Refund Succeeded

Occurs when a payment refund is confirmed as succeeded.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_refund_payload:  # WebhookRefundPayload | 
}

begin
  # Refund Succeeded
  api_instance.refund_succeeded_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->refund_succeeded_post: #{e}"
end
```

#### Using the refund_succeeded_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> refund_succeeded_post_with_http_info(opts)

```ruby
begin
  # Refund Succeeded
  data, status_code, headers = api_instance.refund_succeeded_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->refund_succeeded_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_refund_payload** | [**WebhookRefundPayload**](WebhookRefundPayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## subscription_created_post

> subscription_created_post(opts)

Subscription Created

Occurs when a customer subscription is successfully started.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_subscription_payload:  # WebhookSubscriptionPayload | 
}

begin
  # Subscription Created
  api_instance.subscription_created_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->subscription_created_post: #{e}"
end
```

#### Using the subscription_created_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> subscription_created_post_with_http_info(opts)

```ruby
begin
  # Subscription Created
  data, status_code, headers = api_instance.subscription_created_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->subscription_created_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_subscription_payload** | [**WebhookSubscriptionPayload**](WebhookSubscriptionPayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## subscription_deactivated_post

> subscription_deactivated_post(opts)

Subscription Deactivated

Occurs when a customer subscription is deactivated or expired.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_subscription_payload:  # WebhookSubscriptionPayload | 
}

begin
  # Subscription Deactivated
  api_instance.subscription_deactivated_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->subscription_deactivated_post: #{e}"
end
```

#### Using the subscription_deactivated_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> subscription_deactivated_post_with_http_info(opts)

```ruby
begin
  # Subscription Deactivated
  data, status_code, headers = api_instance.subscription_deactivated_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->subscription_deactivated_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_subscription_payload** | [**WebhookSubscriptionPayload**](WebhookSubscriptionPayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## subscription_updated_post

> subscription_updated_post(opts)

Subscription Updated

Occurs when a customer subscription is updated (e.g., cancel at period end changes).

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::DefaultApi.new
opts = {
  webhook_subscription_payload:  # WebhookSubscriptionPayload | 
}

begin
  # Subscription Updated
  api_instance.subscription_updated_post(opts)
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->subscription_updated_post: #{e}"
end
```

#### Using the subscription_updated_post_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> subscription_updated_post_with_http_info(opts)

```ruby
begin
  # Subscription Updated
  data, status_code, headers = api_instance.subscription_updated_post_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue Solifyn::ApiError => e
  puts "Error when calling DefaultApi->subscription_updated_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_subscription_payload** | [**WebhookSubscriptionPayload**](WebhookSubscriptionPayload.md) |  | [optional] |

### Return type

nil (empty response body)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

