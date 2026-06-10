# Solifyn::ProductUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Product display name. | [optional] |
| **description** | **String** | A description of the product. | [optional] |
| **price** | **Float** | Price value. | [optional] |
| **currency** | **String** | Product pricing currency. | [optional][default to &#39;USD&#39;] |
| **image_url** | **String** | URL of the product cover image. | [optional] |
| **tax_category** | **String** | Tax classification. | [optional] |
| **discount** | **Float** | Percentage or flat rate discount. | [optional] |
| **has_license_key** | **Boolean** | Whether to automatically issue license keys upon successful orders. | [optional][default to false] |
| **has_digital_delivery** | **Boolean** | Whether the purchase includes downloadable files. | [optional][default to false] |
| **has_github_access** | **Boolean** | Whether the purchase includes GitHub repository access. | [optional][default to false] |
| **github_repo** | **String** | GitHub repository to grant access to (format: owner/repo). | [optional] |
| **github_permission** | **String** | GitHub collaborator permission level. | [optional] |
| **is_tax_inclusive** | **Boolean** | Whether tax is included in the base price. | [optional][default to false] |
| **activation_limit** | **Integer** | Maximum concurrent activated instances allowed per license key. | [optional] |
| **brand_id** | **String** | Brand id for the product, if not provided will default to primary brand. | [optional] |
| **billing_period** | **Integer** | Billing period in days (for Subscription products). | [optional] |
| **trial_period_days** | **Integer** | Trial duration in days. | [optional] |
| **expiration_days** | **Integer** | Subscription expiration duration in days. | [optional] |
| **statement_descriptor** | **String** | Custom billing descriptor. | [optional] |
| **pay_what_you_want** | **Boolean** | Allow pay-what-you-want pricing. | [optional][default to false] |
| **metadata** | **Hash&lt;String, String&gt;** | Developer key-value metadata pairs. | [optional] |
| **custom_fields** | [**Array&lt;ProductCreateCustomFieldsInner&gt;**](ProductCreateCustomFieldsInner.md) | Form field configurations to gather during checkout. | [optional] |
| **stock** | **Integer** | Initial stock quantity limit. | [optional] |
| **is_listed** | **Boolean** | Whether the product is publicly visible. | [optional][default to true] |
| **is_free** | **Boolean** | Whether the product is free of charge. | [optional][default to false] |
| **addons** | [**Array&lt;ProductCreateAddonsInner&gt;**](ProductCreateAddonsInner.md) | Product addons configurations. | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::ProductUpdate.new(
  name: Enterprise SaaS Plan,
  description: Unlock premium API integration, custom webhooks, dedicated server bandwidth, and priority 24/7 business-critical support tiers.,
  price: 99,
  currency: USD,
  image_url: https://assets.solifyn.com/images/products/saas-enterprise.png,
  tax_category: saas,
  discount: 0,
  has_license_key: false,
  has_digital_delivery: false,
  has_github_access: false,
  github_repo: solifyn/premium-app,
  github_permission: pull,
  is_tax_inclusive: false,
  activation_limit: null,
  brand_id: brd_4e29285b8sdf34ff51e07d4,
  billing_period: 30,
  trial_period_days: 7,
  expiration_days: null,
  statement_descriptor: SOLIFYN*SAAS,
  pay_what_you_want: false,
  metadata: {&quot;internal_id&quot;:&quot;12345&quot;,&quot;campaign&quot;:&quot;summer_sale&quot;},
  custom_fields: [{&quot;id&quot;:&quot;57aa2241-eae4-43dc-b9ae-36069b84b2da&quot;,&quot;name&quot;:&quot;Discord Username&quot;,&quot;order&quot;:0,&quot;required&quot;:true,&quot;field_type&quot;:&quot;text&quot;,&quot;placeholder&quot;:&quot;e.g. your_discord#1234&quot;},{&quot;id&quot;:&quot;c86da32a-a967-457c-815b-c3440294d70b&quot;,&quot;name&quot;:&quot;Company Name&quot;,&quot;order&quot;:1,&quot;required&quot;:false,&quot;field_type&quot;:&quot;text&quot;,&quot;placeholder&quot;:&quot;e.g. Acme Corp (Optional)&quot;}],
  stock: 100,
  is_listed: true,
  is_free: false,
  addons: null
)
```

