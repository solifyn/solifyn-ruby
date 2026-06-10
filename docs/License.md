# Solifyn::License

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique prefix-based identifier of the license key. |  |
| **key** | **String** | The cryptographically generated license key string delivered to the customer. |  |
| **status** | **String** | Lifecycle status of the license. ACTIVE &#x3D; active. DISABLED &#x3D; suspended. REVOKED &#x3D; hard-revoked. |  |
| **business_id** | **String** | The unique identifier associated with the business this license belongs to. |  |
| **product_id** | **String** | The unique ID of the product this license key is associated with. |  |
| **payment_id** | **String** | The unique payment identifier that triggered the issuance of this license key. |  |
| **customer_id** | **String** | The unique customer identifier (ID) who received this license key. |  |
| **activation_limit** | **Float** | Maximum number of simultaneous active device instances allowed for this license. Null means unlimited. |  |
| **activation_message** | **String** | Optional message displayed to the customer upon successful activation. |  |
| **instances_count** | **Float** | Running count of how many times this license key has been activated. |  |
| **expiry_hours** | **Float** | Relative expiry duration in hours from the time of issuance. |  |
| **expires_at** | **String** | Absolute expiration timestamp. The license becomes invalid after this point. |  |
| **filters** | **Object** | Optional custom metadata filters associated with the license. |  |
| **archived** | **Boolean** | Indicates if the license key is archived. |  |
| **created_at** | **String** | Timestamp indicating exactly when the license key was issued. |  |
| **updated_at** | **String** | Timestamp indicating when the license key was last modified. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::License.new(
  id: lic_hyQQhhNzfEuvv,
  key: A184-99C2-8CBE,
  status: ACTIVE,
  business_id: biz_345TUESrCDPvrb,
  product_id: prod_hyQQhhNzfEuvv,
  payment_id: pay_3r2FgHXp9,
  customer_id: cust_3r2FgHXp9,
  activation_limit: 3,
  activation_message: Thank you! Your license is now active.,
  instances_count: 1,
  expiry_hours: 720,
  expires_at: 2027-01-01T00:00:00.000Z,
  filters: null,
  archived: false,
  created_at: 2026-05-11T01:12:25.764Z,
  updated_at: 2026-05-18T09:45:37.166Z
)
```

