## Frequently Asked Questions

### How to preserve client IP addresses on the HDT platform?
You can configure HDT to preserve client IP addresses using the HDT web portal.

For HTTP/HTTPS applications, the X-Forwarded-For (XFF) HTTP header is enabled by default. For other applications, you can enable the preservation of client IP addresses in the [Edit a Transport](</docs/portal/transports/edit-transport.md>) page.

![null](</docs/resources/images/faq/faq-preserveClientIP-1.png>)

For more information, see the blog [How to preserve client IP addresses on the HDT platform](<https://www.{{siteDomain}}/enterprise-applications-blog/how-to-preserve-client-ip-addresses-on-the-hdt-platform/>), which describes how HDT sends client information to the origin server.

For technical assistance regarding the preservation of client IP addresses on the HDT platform, or for help installing or configuring the TCP option module on your origin server, please contact our [HDT support team](mailto:support@{{siteDomain}}), We welcome your inquiries and look forward to helping you meet your requirements. 
