# Solifyn::PayoutsApi

All URIs are relative to *http://localhost:8000*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**payouts_create_withdrawal**](PayoutsApi.md#payouts_create_withdrawal) | **POST** /v1/payouts/withdrawals | Create Withdrawal |
| [**payouts_get_account**](PayoutsApi.md#payouts_get_account) | **GET** /v1/payouts/account | Retrieve Payout Account |
| [**payouts_get_account_link**](PayoutsApi.md#payouts_get_account_link) | **GET** /v1/payouts/account-link | Create Account Link |
| [**payouts_get_token**](PayoutsApi.md#payouts_get_token) | **GET** /v1/payouts/token | Generate Portal Access Token |
| [**payouts_get_withdrawals**](PayoutsApi.md#payouts_get_withdrawals) | **GET** /v1/payouts/withdrawals | Get Withdrawals List |
| [**payouts_list_methods**](PayoutsApi.md#payouts_list_methods) | **GET** /v1/payouts/methods | List Payout Methods |
| [**payouts_list_verifications**](PayoutsApi.md#payouts_list_verifications) | **GET** /v1/payouts/verifications | List Verifications |
| [**payouts_list_withdrawals**](PayoutsApi.md#payouts_list_withdrawals) | **GET** /v1/payouts | List Withdrawals |


## payouts_create_withdrawal

> <Withdrawal> payouts_create_withdrawal(withdrawal_create)

Create Withdrawal

Initiate a balance withdrawal transfer request.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::PayoutsApi.new
withdrawal_create = Solifyn::WithdrawalCreate.new({amount: 1000, currency: 'usd'}) # WithdrawalCreate | 

begin
  # Create Withdrawal
  result = api_instance.payouts_create_withdrawal(withdrawal_create)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_create_withdrawal: #{e}"
end
```

#### Using the payouts_create_withdrawal_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<Withdrawal>, Integer, Hash)> payouts_create_withdrawal_with_http_info(withdrawal_create)

```ruby
begin
  # Create Withdrawal
  data, status_code, headers = api_instance.payouts_create_withdrawal_with_http_info(withdrawal_create)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <Withdrawal>
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_create_withdrawal_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **withdrawal_create** | [**WithdrawalCreate**](WithdrawalCreate.md) |  |  |

### Return type

[**Withdrawal**](Withdrawal.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## payouts_get_account

> <PayoutAccount> payouts_get_account

Retrieve Payout Account

Retrieve general status and information of onboarding payout accounts.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::PayoutsApi.new

begin
  # Retrieve Payout Account
  result = api_instance.payouts_get_account
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_get_account: #{e}"
end
```

#### Using the payouts_get_account_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayoutAccount>, Integer, Hash)> payouts_get_account_with_http_info

```ruby
begin
  # Retrieve Payout Account
  data, status_code, headers = api_instance.payouts_get_account_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayoutAccount>
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_get_account_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**PayoutAccount**](PayoutAccount.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## payouts_get_account_link

> <PayoutAccountLink> payouts_get_account_link(opts)

Create Account Link

Generate temporary links for onboarding or viewing portals.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::PayoutsApi.new
opts = {
  use_case: 'account_onboarding' # String | Onboarding link type context
}

begin
  # Create Account Link
  result = api_instance.payouts_get_account_link(opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_get_account_link: #{e}"
end
```

#### Using the payouts_get_account_link_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayoutAccountLink>, Integer, Hash)> payouts_get_account_link_with_http_info(opts)

```ruby
begin
  # Create Account Link
  data, status_code, headers = api_instance.payouts_get_account_link_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayoutAccountLink>
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_get_account_link_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **use_case** | **String** | Onboarding link type context | [optional] |

### Return type

[**PayoutAccountLink**](PayoutAccountLink.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## payouts_get_token

> <PayoutAccessToken> payouts_get_token

Generate Portal Access Token

Generate temporary credentials to access the embed portal.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::PayoutsApi.new

begin
  # Generate Portal Access Token
  result = api_instance.payouts_get_token
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_get_token: #{e}"
end
```

#### Using the payouts_get_token_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayoutAccessToken>, Integer, Hash)> payouts_get_token_with_http_info

```ruby
begin
  # Generate Portal Access Token
  data, status_code, headers = api_instance.payouts_get_token_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayoutAccessToken>
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_get_token_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**PayoutAccessToken**](PayoutAccessToken.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## payouts_get_withdrawals

> <WithdrawalList> payouts_get_withdrawals(opts)

Get Withdrawals List

Retrieve withdrawal records for the active business.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::PayoutsApi.new
opts = {
  limit: 8.14, # Float | Page size limit
  page: 8.14 # Float | Page number
}

begin
  # Get Withdrawals List
  result = api_instance.payouts_get_withdrawals(opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_get_withdrawals: #{e}"
end
```

#### Using the payouts_get_withdrawals_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WithdrawalList>, Integer, Hash)> payouts_get_withdrawals_with_http_info(opts)

```ruby
begin
  # Get Withdrawals List
  data, status_code, headers = api_instance.payouts_get_withdrawals_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WithdrawalList>
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_get_withdrawals_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Float** | Page size limit | [optional] |
| **page** | **Float** | Page number | [optional] |

### Return type

[**WithdrawalList**](WithdrawalList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## payouts_list_methods

> <PayoutMethodList> payouts_list_methods(opts)

List Payout Methods

List saved payout destinations (bank accounts, cards).

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::PayoutsApi.new
opts = {
  limit: 8.14, # Float | 
  page: 8.14 # Float | 
}

begin
  # List Payout Methods
  result = api_instance.payouts_list_methods(opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_list_methods: #{e}"
end
```

#### Using the payouts_list_methods_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayoutMethodList>, Integer, Hash)> payouts_list_methods_with_http_info(opts)

```ruby
begin
  # List Payout Methods
  data, status_code, headers = api_instance.payouts_list_methods_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayoutMethodList>
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_list_methods_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Float** |  | [optional] |
| **page** | **Float** |  | [optional] |

### Return type

[**PayoutMethodList**](PayoutMethodList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## payouts_list_verifications

> <PayoutVerificationList> payouts_list_verifications(opts)

List Verifications

Retrieve pending or completed KYC verification checks.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::PayoutsApi.new
opts = {
  limit: 8.14, # Float | 
  page: 8.14 # Float | 
}

begin
  # List Verifications
  result = api_instance.payouts_list_verifications(opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_list_verifications: #{e}"
end
```

#### Using the payouts_list_verifications_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PayoutVerificationList>, Integer, Hash)> payouts_list_verifications_with_http_info(opts)

```ruby
begin
  # List Verifications
  data, status_code, headers = api_instance.payouts_list_verifications_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PayoutVerificationList>
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_list_verifications_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Float** |  | [optional] |
| **page** | **Float** |  | [optional] |

### Return type

[**PayoutVerificationList**](PayoutVerificationList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## payouts_list_withdrawals

> <WithdrawalList> payouts_list_withdrawals(opts)

List Withdrawals

Retrieve a list of past withdrawal history.

### Examples

```ruby
require 'time'
require 'solifyn'
# setup authorization
Solifyn.configure do |config|
  # Configure Bearer authorization (API Key): ApiKeyAuth
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = Solifyn::PayoutsApi.new
opts = {
  limit: 8.14, # Float | Page size limit
  page: 8.14 # Float | Page number
}

begin
  # List Withdrawals
  result = api_instance.payouts_list_withdrawals(opts)
  p result
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_list_withdrawals: #{e}"
end
```

#### Using the payouts_list_withdrawals_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WithdrawalList>, Integer, Hash)> payouts_list_withdrawals_with_http_info(opts)

```ruby
begin
  # List Withdrawals
  data, status_code, headers = api_instance.payouts_list_withdrawals_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WithdrawalList>
rescue Solifyn::ApiError => e
  puts "Error when calling PayoutsApi->payouts_list_withdrawals_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Float** | Page size limit | [optional] |
| **page** | **Float** | Page number | [optional] |

### Return type

[**WithdrawalList**](WithdrawalList.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

