# Two-factor authentication

You can enhance the security of user accounts on the Navixy platform by enabling Two-Factor Authentication (2FA). You can configure this security feature for all users or selectively enable it based on specific account needs.

### **How to enable 2FA for users**

1. **Enabling for all users**: to enforce 2FA across the entire platform, navigate to _Admin Panel → Account management → Security._ This ensures that all current and new users must authenticate using a one-time passcode in addition to their login credentials. All sub-users and imported users will also inherit the 2FA settings. Note that 2FA settings do not apply to demo users.
2. **Enabling for specific users**: for individual accounts that require personalized security, go to _Admin Panel → Users → Edit user → Two-factor authentication._ Here, you can enable or disable 2FA for specific accounts based on their security requirements. All sub-users, created in that account, will also inherit the 2FA settings.&#x20;

![Screenshot 2024-09-18 at 14.19.29.png](<attachments/Screenshot 2024-09-18 at 14.19.29.png>)

{% hint style="info" %}
Note that the current implementation only allows enabling Two-Factor Authentication for all account users, including sub-users created in the main account.
{% endhint %}

To configure 2FA settings, you can utilize our updated Panel API, using the calls to read and update 2FA settings for a list of specified users or all users of the platform, as well as set default settings for new users. You can learn more about our Panel API in the [Developer Hub](https://app.gitbook.com/s/6dtcPLayxXVB2qaaiuIL/panel-api/resources/user/mfa-settings).
