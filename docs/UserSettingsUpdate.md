# Solifyn::UserSettingsUpdate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subdomain** | **String** | The custom store subdomain | [optional] |
| **store_name** | **String** | The store name shown to customers | [optional] |
| **social_links** | **Object** | JSON structure listing social/contact URLs | [optional] |
| **page_title** | **String** | SEO title tag of the store page | [optional] |
| **seo_description** | **String** | SEO description meta tag | [optional] |
| **seo_image** | **String** | SEO preview image URL | [optional] |
| **favicon_url** | **String** | Favicon image URL | [optional] |
| **google_analytics_id** | **String** | Google Analytics 4 Property ID | [optional] |
| **google_tag_manager_id** | **String** | Google Tag Manager Container ID | [optional] |
| **meta_pixel_id** | **String** | Facebook Meta Pixel ID | [optional] |
| **logo_url** | **String** | Company/Store logo image URL | [optional] |
| **business_title** | **String** | Name of the business entity | [optional] |
| **statement_descriptor** | **String** | Credit card statement descriptor | [optional] |
| **default_currency** | **String** | Three-letter currency symbol | [optional] |
| **email** | **String** | User contact email | [optional] |
| **first_name** | **String** | User first name | [optional] |
| **last_name** | **String** | User last name | [optional] |
| **avatar_url** | **String** | User profile avatar URL | [optional] |
| **payout_threshold** | **Float** | Minimum balance required for automatic payouts in cents | [optional] |
| **notify_on_success** | **Boolean** | Send email notifications on successful payments | [optional] |
| **send_license_key_email** | **Boolean** | Send license keys automatically via email | [optional] |
| **send_digital_file_email** | **Boolean** | Send download links automatically via email | [optional] |
| **notify_on_subscription_plan_changed** | **Boolean** | Send email notifications on subscription plan changes | [optional] |
| **notify_on_subscription_set_to_cancel** | **Boolean** | Send email notifications when subscription is set to cancel | [optional] |
| **notify_on_subscription_cancelled** | **Boolean** | Send email notifications when subscription is cancelled | [optional] |
| **notify_on_refund_successful** | **Boolean** | Send email notifications when refund is successful | [optional] |
| **notify_on_payment_failed** | **Boolean** | Send email notifications when payment fails | [optional] |
| **notify_on_subscription_renewal_failed** | **Boolean** | Send email notifications when subscription renewal fails | [optional] |
| **notify_on_subscription_trial_ending** | **Boolean** | Send email notifications when subscription trial is ending | [optional] |
| **notify_on_subscription_paused** | **Boolean** | Send email notifications when subscription is paused | [optional] |

## Example

```ruby
require 'solifyn'

instance = Solifyn::UserSettingsUpdate.new(
  subdomain: acme,
  store_name: Acme Store,
  social_links: null,
  page_title: Acme - Shop,
  seo_description: Buy Acme products here,
  seo_image: https://acme.com/seo.png,
  favicon_url: https://acme.com/favicon.ico,
  google_analytics_id: G-XXXXXX,
  google_tag_manager_id: GTM-XXXXXX,
  meta_pixel_id: 1234567890,
  logo_url: https://acme.com/logo.png,
  business_title: Acme Inc,
  statement_descriptor: ACME SHOP,
  default_currency: USD,
  email: contact@acme.com,
  first_name: John,
  last_name: Doe,
  avatar_url: https://acme.com/profile.png,
  payout_threshold: 5000,
  notify_on_success: true,
  send_license_key_email: true,
  send_digital_file_email: true,
  notify_on_subscription_plan_changed: true,
  notify_on_subscription_set_to_cancel: true,
  notify_on_subscription_cancelled: true,
  notify_on_refund_successful: true,
  notify_on_payment_failed: true,
  notify_on_subscription_renewal_failed: true,
  notify_on_subscription_trial_ending: true,
  notify_on_subscription_paused: true
)
```

