# Solifyn::Product

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | The unique identifier (ID) of the product. |  |
| **name** | **String** | The display name of the product. |  |
| **price** | **Float** | The price amount of the product (e.g. 29.00). |  |
| **currency** | **String** | The three-letter ISO currency code (e.g. USD, VND, EUR). |  |
| **description** | **String** | A comprehensive rich text description of the product. | [optional] |
| **status** | **String** | The lifecycle status of the product (e.g. ACTIVE, ARCHIVED). |  |
| **image_url** | **String** | URL of the product cover image. |  |
| **tax_category** | **String** | The tax classification for the product. |  |
| **pricing_type** | **String** | Pricing model of the product. |  |
| **discount** | **Float** | Discount value as a percentage or fixed amount. |  |
| **has_license_key** | **Boolean** | Indicates if the product issues a cryptographically secure software license key upon checkout completion. |  |
| **has_digital_delivery** | **Boolean** | Whether the product includes digital file downloads upon purchase. |  |
| **is_tax_inclusive** | **Boolean** | Whether the product price already includes applicable sales taxes. |  |
| **billing_period** | **Integer** | The subscription billing cycle interval in days (for subscription products). |  |
| **trial_period_days** | **Integer** | Trial duration in days for subscription products. |  |
| **expiration_days** | **Integer** | Automatic expiration period in days for the subscription entitlement. |  |
| **statement_descriptor** | **String** | Custom text displayed on customer credit card statements for purchases of this product. |  |
| **pay_what_you_want** | **Boolean** | Indicates if customers are allowed to enter a custom pricing amount at checkout. |  |
| **metadata** | **Hash&lt;String, String&gt;** | Custom developer metadata key-value pairs associated with the product. |  |
| **custom_fields** | **Array&lt;Object&gt;** | Custom form field questions to ask the customer during checkout. |  |
| **stock** | **Integer** | Available stock quantity, or null for unlimited inventory. |  |
| **activation_limit** | **Integer** | Maximum number of simultaneous active instances/devices allowed per issued license key (applicable if hasLicenseKey is true). |  |
| **is_listed** | **Boolean** | Defines if the product is listed publicly on the merchant&#39;s storefront template. |  |
| **created_at** | **Time** | Timestamp indicating exactly when the product was created. |  |
| **updated_at** | **Time** | Timestamp indicating when the product was last modified. |  |
| **is_permanently_deleted** | **Boolean** | Indicates if the product has been permanently deleted. |  |
| **brand_id** | **String** | Optional brand identifier. |  |
| **digital_link** | **String** | Secure link for digital delivery. |  |
| **instructions** | **String** | Special instructions provided upon purchase. |  |
| **activation_message** | **String** | Custom message displayed when a license key is activated. |  |
| **expiry_hours** | **Integer** | Number of hours until the license key expires. |  |
| **business_id** | **String** | The unique identifier of the business owning this product. |  |

## Example

```ruby
require 'solifyn'

instance = Solifyn::Product.new(
  id: prod_9z8x7c6v5b4n,
  name: Enterprise SaaS Plan,
  price: 99,
  currency: USD,
  description: Unlock premium API integration, custom webhooks, dedicated server bandwidth, and priority 24/7 business-critical support tiers.,
  status: ACTIVE,
  image_url: https://assets.solifyn.com/images/products/saas-enterprise.png,
  tax_category: saas,
  pricing_type: one_time,
  discount: 0,
  has_license_key: true,
  has_digital_delivery: false,
  is_tax_inclusive: false,
  billing_period: null,
  trial_period_days: null,
  expiration_days: null,
  statement_descriptor: SOLIFYN*SAAS,
  pay_what_you_want: false,
  metadata: {tier&#x3D;enterprise, department&#x3D;engineering},
  custom_fields: [{id&#x3D;57aa2241-eae4-43dc-b9ae-36069b84b2da, name&#x3D;Discord Username, order&#x3D;0, required&#x3D;true, field_type&#x3D;text, placeholder&#x3D;e.g. your_discord#1234}, {id&#x3D;c86da32a-a967-457c-815b-c3440294d70b, name&#x3D;Company Name, order&#x3D;1, required&#x3D;false, field_type&#x3D;text, placeholder&#x3D;e.g. Acme Corp (Optional)}],
  stock: null,
  activation_limit: 5,
  is_listed: true,
  created_at: 2026-05-18T12:00:00.000Z,
  updated_at: 2026-05-18T12:00:00.000Z,
  is_permanently_deleted: false,
  brand_id: brd_4e29285b8sdf34ff51e07d4,
  digital_link: null,
  instructions: Log in to your Solifyn developer dashboard and enter your license key to activate the premium SaaS resources.,
  activation_message: Activation successful. Welcome to the Solifyn Enterprise Plan!,
  expiry_hours: 8760,
  business_id: biz_4r5t6y7u8i9o
)
```

