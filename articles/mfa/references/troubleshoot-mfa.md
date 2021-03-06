---
description: Describes basic troubleshooting of MFA issues for end-users.
topics:
    - mfa
contentType:
  - reference
useCase:
  - customize-mfa
---
# Troubleshoot Multi-Factor Authentication

This guide serves as a troubleshooting reference if you have end-users unable to log in with <dfn data-key="multifactor-authentication">multi-factor authentication (MFA)</dfn>.

## Generic issues

### If you do not have your mobile device, or your mobile device is turned off

If you have lost your device, you can finish authentication using the recovery code provided when you first signed up. 

1. Enter your email and password to log in, and click the **Use the recovery code** link.
2. Enter your recovery code.

If you no longer have your recovery code, you will not be able to log in. Contact your system administrator for help accessing your account.

### If you forget your password

If you have forgotten your password, click the **Don't remember your password?** link located underneath the email and password fields. Then, enter your email address to receive an email containing a link you can use to reset your password.

### If your transaction expires

When logging in via MFA, there is a five-minute maximum between providing your first and second factors. You can see how much time has elapsed since you logged in using the first factor by checking the timestamp on the messages provided.

If more than five minutes has elapsed, you will need to log in again and obtain a new code or notification.

If you are requesting SMS or Voice messages, make sure you are not [exceeding rate limits](#sms-rate-limits).

### If you need to remove or delete MFA from a user in your tenant

If you need to remove, delete, or reset MFA for a user, you should [reset MFA](/mfa/guides/reset-user-mfa).

## Phone messaging-related issues

### SMS message rate limits

If a user attempts to send more than ten SMS or Voice messages within one hour, they will see an error message saying so.

When they exceed your messaging limit, they'll need to wait at least an hour after they sent the first message before sending another. They will receive an additional attempt after the passage of each additional hour.

## Rejected Codes

If the 6-digit code in the Guardian or the Google Authenticator app are being rejected for sign in (often with the message `Incorrect Code`), first check that you are selecting the right application from the list in your authenticator app. If you've verified that you're selecting the correct application, make sure that your mobile device's clock settings are correct. One-time passwords are generated using Coordinated Universal Time (UTC), so your device's time must be correct for your code to work.

To check your clock settings:

* **Android Devices** - Go **Settings** > **Date & Time**. Make sure that the box next to **Automatic** is checked.

* **iOS Devices** - Go to  **Settings** > **General** > **Date & Time**. Enable **Set Automatically**. If this setting was already enabled, you can disable it for a moment, then re-enable.

## Duo-related issues

For questions or issues specifically regarding Duo, [see Duo's documentation](https://guide.duo.com).

Android, then tap "Settings." Scroll down to the bottom of the Settings menu, then tap "Date & Time." Tap the box next to "Automatic" to un-check it.
