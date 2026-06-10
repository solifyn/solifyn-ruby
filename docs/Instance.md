# Solifyn::Instance

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique database identifier of this instance record. |  |
| **license_id** | **String** | The internal ID of the parent license key this instance belongs to. |  |
| **instance_id** | **String** | The unique hardware hash or client-generated identifier of the activated device/machine. |  |
| **instance_name** | **String** | A human-readable display name for this instance, assigned by the client application. |  |
| **ip_address** | **String** | The IP address recorded at the time of activation. |  |
| **activated_at** | **String** | Timestamp when this device instance was first activated. |  |
| **last_seen_at** | **String** | Timestamp of the most recent activation heartbeat or re-activation check from this device. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::Instance.new(
  id: 7f3a1b2c-4d5e-6f7a-8b9c-0d1e2f3a4b5c,
  license_id: lic_hyQQhhNzfEuvv,
  instance_id: machine-ID-abc123,
  instance_name: MacBook Pro 16&quot;,
  ip_address: 203.0.113.42,
  activated_at: 2026-05-15T10:30:00.000Z,
  last_seen_at: 2026-05-18T08:00:00.000Z
)
```

