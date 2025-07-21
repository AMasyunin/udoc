# Email gateway

There are a number of situations where GPS tracking system users receive automated emails. Examples include:

* Event notifications (if email notification is selected)
* Excel / PDF reports by customized schedule
* Notifications about the need to top up the balance, etc.

In this case, you, as the service operator, can define through which Email gateway the mail will be delivered, as well as set the sender's address (the 'from' field).

### **Selecting an Email Gateway**

Depending on the type of Navixy product you use and your preferences, you can choose between two options:

* **Navixy Email Gateway** - available and free for all ServerMate users. The gateway is organized on the basis of mandrill service, which provides email delivery with high speed and guarantee. So if you are using Navixy ServerMate product, this is the recommended option.
* **Your SMTP gateway** is an option available to users of all products: ServerMate, Cloud and On-Premise. This is a universal method where you specify through which server email messages will be delivered: your own SMTP server, any of the public services (i.e Gmail, etc.) or a specialized one (mandrill, sendgrid, mailgun, etc.).

### **Selecting the sender address**

You can choose which address will be specified in the 'From' field as the sender's address and set it in the Administrator panel. The most common address is 'no-reply@yourdomain.com', where yourdomain.com is the domain where your GPS monitoring service is running.

However, in order for SPAM filters not to block automated messages and for emails to be delivered to users with a high guarantee, the sender's address must fulfill certain requirements (see the links above in the relevant sections for details).

## **Navixy Gateway**

Navixy Email Gateway is available and free for all ServerMate users. The gateway is organized based on Mandrill, which ensures email delivery with high speed and guarantee. So if you are using the Navixy ServerMate product, this is the recommended option.

By default, the 'From' field (sender address) is set to 'no-reply@x-gpsmail.com'. In this default case, you don't need to make any special settings and mail will be guaranteed to be delivered to users.

If you want to specify your address in the 'From' field as well, you need to authorize your domain for mail delivery. Only then will your address be used and your emails will be guaranteed to be skipped by spam filters.

#### **Your Own 'From' Address**

Setting up your own sender address (the 'From' field) is done in three steps: (1), Authenticating your domain (2) Authorizing the domain and (3) assigning the sender address.

#### **Step 1: Authenticating your domain**

For this you need to reach out to Navixy Support ([support@navixy.com](mailto:support@navixy.com)) and provide the name of the domain you are going to use for outgoing e-mail. This doesn’t need to be the same as your platform’s domain, however it needs to be one that you have access to make DNS changes to. Once you reach out to Support with your domain, you will receive a TXT record to add to your DNS which proves to the World Wide Web that you own the domain and will allow Mandrill to use it to send outgoing emails. The record will look similar to the below, with “yourdomain.com” being the domain you provided, and KEY\_PROVIDED\_HERE being the key Support gives you:

`yourdomain.com. 1 IN TXT "mandrill_verify.KEY_PROVIDED_HERE"`

This is done within the DNS settings provided by your DNS provider. Every DNS provider has their own tools and way their settings look. If you need assistance adding the records in question, please reach out to your DNS provider.

#### **Step 2: Authorizing your domain**

The second change you need to make is to add four more DNS records for your domain: one SPF, two DKIM, and one DMARC record.

**SPF field.**\
You need to create a new TXT record or update your existing SPF TXT record on your domain:

if you have no SPF configured on your domain, simply publish the following TXT record on it:

`v=spf1 include:spf.mandrillapp.com -all`

if you already have an SPF record, simply insert `include:spf.mandrillapp.com` right before the terminating mechanism in that record.

For example, if your current SPF record looks like this:

`v=spf1 a -all`

update it to:

`v=spf1 a include:spf.mandrillapp.com -all`

**DKIM field.** Create two CNAME records for your domain: one with the name `mte1._domainkey.yourdomain.com` with the value `dkim1.mandrillapp.com`, and another with the name `mte2._domainkey.yourdomain.com` and the value `dkim2.mandrillapp.com` **Replacing “yourdomain.com” with your associated domain name.**

**DMARC field.** Create and save a TXT record in your DNS with a name of `_dmarc.yourdomain.com` and a value of `v=DMARC1; p=none;` **Replacing “yourdomain.com” with your associated domain name.**

After creating the records, remember to save the DNS information. It then takes 30 minutes or up to 4 hours to propagate the settings out to the Internet, so you should wait before proceeding to the next step.

#### **Step 3: Assigning the sender address**

After some time has passed and the fields you have created in the DNS record have propagated, you can assign Navixy's 'From' field value to an address that is convenient for you (like \*@yourdomain.com).

To do this, write an e-mail to the technical support service ([support@navixy.com](mailto:support@navixy.com)), specify your admin panel login and the desired e-mail address. Support specialists will promptly set up and test sending messages from the specified address, after which they will inform you about the completion of the settings by e-mail.

#### **How to check if the DKIM field is correct**

After all the settings have been made, the user should receive emails with a confirmed digital signature. You can check this by sending a test message to your personal email. In the received message, select "Show original" and try to find _dkim=pass_ - finding this means that the field is configured correctly. Otherwise, the message is either not signed or the signature is incorrect.

## **3rd party gateway**

With all Navixy products (ServerMate, Cloud and On-Premise), you can use an arbitrary SMTP server for mail delivery.

It can be your own daemon service, public mail service (i.e. Gmail) or specialized guaranteed message delivery service (mandrill, sendgrid, mailgun, etc.). In all these cases you need to specify access details to the SMTP server.

To configure it, log in to the administrator panel and go to the "Site Settings" section. In the "Email messages" subsection, select "Your SMTP server". Specify whether you use a secure data transfer protocol, after that the SMTP port field will be filled in automatically in accordance with the recommendations for configuring public email services. If necessary, you can change the SMTP port number manually. You can find out the SMTP server address when using public email services in the support section of the corresponding service, for example, for the gmail server the settings are available [here](https://support.google.com/a/answer/176600?hl=ru).

If the server you are using asks for authorization, tick the appropriate checkbox and provide a login and password. Public email services usually do not require a login and password for authorization on the server.

After entering the SMTP server settings, specify the email on behalf of which notifications will be sent and the signature that will be automatically inserted into each email.

Now save the settings, the window will look something like the one in the screenshot.

To check the correctness of the setting use sending a test email, click the "Send Test Email" button and specify the address to which you want to send it.

If the setting is correct, a test email will be sent to the specified address.
