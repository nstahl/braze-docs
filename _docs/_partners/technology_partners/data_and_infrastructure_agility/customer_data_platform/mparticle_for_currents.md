---
nav_title: mParticle for Currents
page_order: 0.5
alias: /partners/mparticle_for_currents/
---

# About mParticle & Currents

[mParticle](https://www.mparticle.com) is a customer data platform that collects and routes information from multiple sources to a variety of other locations in your marketing stack.

To get started, find the following information from your mParticle dashboard:

-   mParticle Server to Server Key
-   mParticle Server to Server Secret

Add this information to the mParticle integration page on the dashboard, and press save.

![mParticle]({% image_buster /assets/img_archive/currents-mparticle-edit.png %})

All events sent to mParticle will include the user's `external_user_id` as the `customerid`. At this time, Braze does not send event data for users who do not have their `external_user_id` set.

mParticle's documentation is available [here](http://docs.mparticle.com/integrations/braze/feed).

# Integration Details

You can export the following data from Braze to mParticle:

| Event Name                           | Feed Type              | Description                                                                               | Custom Attributes
| ------------------------------------ | ---------------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| Push Notification Send               | Platform-specific Feed | A push notification was successfully sent to a User.                                      | `app_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`             |
| Push Notification Open               | Platform-specific Feed | User opened a push notification.                                                          | `app_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`             |
| Push Notification Bounce             | Platform-specific Feed | Braze was not able to send a push notification to this User.                              | `app_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`             |
| Email Sent                           | Unbound Feed           | An email was successfully sent.                                                           | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`                      |
| Email Delivered                      | Unbound Feed           | An email was successfully delivered to a User’s mail server.                              | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`                      |
| Email Opened                         | Unbound Feed           | User opened an email.                                                                     | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`                      |
| Email Clicked                        | Unbound Feed           | User clicked a link in an email. Email click tracking must be enabled.                    | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`                      |
| Email Bounced                        | Unbound Feed           | Braze attempted to send an email, but the User’s receiving mail server did not accept it. | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`                      |
| Email Marked As Spam                 | Unbound Feed           | User marked an email as spam.                                                             | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`                      |
| Email Unsubscribed                   | Unbound Feed           | User clicked the unsubscribe link in an email.                                            | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`                      |
| Subscription Group State Change      | Unbound Feed           | User's subscription group state changed to 'Subscribed' or 'Unsubscribed'                 | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`                      |
| In-App Message Impression            | Platform-specific Feed | User viewed an In-App Message.                                                            | `app_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`             |
| In-App Message Clicked               | Platform-specific Feed | User tapped or clicked a button in an In-App Message.                                     | `button_id`, `app_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id` |
| Content Card Sent                    | Platform-specific Feed | A Content Card was sent to a user's device                                                | `app_id`, `card_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`  |
| Content Card Viewed                  | Platform-specific Feed | User viewed a Content Card                                                                | `app_id`, `card_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`  |
| Content Card Clicked                 | Platform-specific Feed | User clicked a Content Card                                                               | `app_id`, `card_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`  |
| Content Card Dismissed               | Platform-specific Feed | User dismissed a Content Card                                                             | `app_id`, `card_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`  |
| News Feed Viewed                     | Platform-specific Feed | User viewed the native Braze News Feed.                                                   | `app_id`, `card_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`  |
| News Feed Card Viewed                | Platform-specific Feed | User viewed a Card within the native Braze News Feed.                                     | `app_id`, `card_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`  |
| News Feed Card Clicked               | Platform-specific Feed | User clicked on a Card within the native Braze News Feed.                                 | `app_id`, `card_id`, `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`  |
| Webhook Sent                         | Unbound Feed           | A webhook message was sent on behalf of a User.                                           | `campaign_id`, `canvas_step_id`, `canvas_id`, `canvas_variation_id`                      |
| Application Uninstalled              | Platform-specific Feed | User uninstalled the App.                                                                 | `app_id`                                                                              |
| Campaign Conversion Event            | Unbound Feed           | User performed the primary conversion event for a Campaign within its conversion window.  | `campaign_id`                                                                         |
| Campaign Enrollment in Control Group | Unbound Feed           | User was enrolled in a Campaign control group.                                            | `campaign_id`                                                                         |
| Canvas Conversion Event              | Unbound Feed           | User performed the primary conversion event for a Canvas within its conversion window.    | `canvas_step_id`, `canvas_id`, `canvas_variation_id`                                    |
| Canvas Entry                         | Unbound Feed           | User was entered into a Canvas.                                                           | `in_control_group`, `canvas_id`, `canvas_variation_id`                                  |
