# Solifyn::UserSettings

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | User ID |  |
| **email** | **String** | Primary email address |  |
| **first_name** | **String** | First name | [optional] |
| **last_name** | **String** | Last name | [optional] |
| **avatar_url** | **String** | Profile avatar image URL | [optional] |
| **payout_threshold** | **Float** | Auto-payout minimum threshold limit in cents |  |
| **notify_on_success** | **Boolean** | Auto-email receipt toggled |  |
| **send_license_key_email** | **Boolean** | Send license keys email automatically |  |
| **send_digital_file_email** | **Boolean** | Send digital delivery download link emails automatically |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::UserSettings.new(
  id: usr_123,
  email: contact@acme.com,
  first_name: John,
  last_name: Doe,
  avatar_url: https://acme.com/avatar.png,
  payout_threshold: 5000,
  notify_on_success: true,
  send_license_key_email: true,
  send_digital_file_email: true
)
```

