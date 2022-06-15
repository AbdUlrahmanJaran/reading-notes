# Sending Email with Microsoft Azure
To do. you have to Create and configure a Twilio SendGrid account using Microsoft Azure.

### What is SendGrid?
> SendGrid is a cloud-based SMTP(Simple Mail Transfer Protocol) provider that allows you to send email without having to maintain email servers. SendGrid manages all of the technical details.

### Create a Twilio SendGrid account
> From the Azure portal home page, select Marketplace under Azure services. If you do not see the Marketplace icon, you can search for it by selecting More services.
Click the Twilio SendGrid resource to load a page where you can select your account tier.

#### Two-factor authentication
> Twilio SendGrid uses Two-factor authentication (2FA) to help protect your account. To enable 2FA, Navigate to Two-Factor Authentication in the Twilio SendGrid Settings menu, and click Add Two-Factor Authentication.

#### API keys
> API Keys authenticate your application, mail client, or website with Twilio SendGrid services. Unlike a username and password, API keys are scoped to provide access only to the services you select. You can also delete and create API keys without impacting your other account credentials. For these reasons, Twilio SendGrid requires you to connect to its services using API keys.

#### Sender Authentication
> Twilio SendGrid requires customers to complete Sender Authentication. This requirement protects your domain's reputation as an email sender and helps uphold legitimate sending behavior by Twilio SendGrid customers.

### Ref: [Twilio SendGrid doc](https://docs.sendgrid.com/for-developers/partners/microsoft-azure-2021#create-a-twilio-sendgrid-account) and [definition](https://sendgrid.com/wp-content/uploads/2016/09/SendGrid-Implementation-Review.pdf).