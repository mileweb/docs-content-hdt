# Add New Transport

The <strong> Transports </strong> page can be reached by clicking "Transports" from the left pane of the HDT portal.
To add a new transport, click the **Add New Transport** button at the top right of the <strong> Transports </strong> page to display the wizard instructions.

## Basic Info
![null](</docs/resources/images/transports/add-transport-basic-info.png>)

| Fields               | Description   |
| -------------------- | ------------- |
| Transport Name       | Enter a name to identify this transport. If you omit this parameter, HDT portal will generate a default name in "Target Domain:Target Port" format|
| Version Number       | Version number of the transport configuration in history. |
| Application Protocol | <strong> HTTP </strong>: For HTTP protocol. <br> <strong> HTTPS </strong>: For HTTPS protocol with SNI (Server Name Indication). |
| IP Version           | IP version supported by your application, IPv4, IPv6, or both. |

## Settings
![null](</docs/resources/images/transports/add-transport-settings-1.png>)

| Fields               | Description   |
| -------------------- | ------------- |
| Fixed Shields        | If select Yes, the shield servers (HDT servers that connect to your origin servers) will be fixed, and you can choose the region of shield servers to be fixed in the drop-down list. |
| Dedicated IP Service | If select Yes, the IP addresses for serving the transport will be dedicated to the CNAME only. The service will NOT be applicable if Application Protocol is HTTP or HTTPS. To use Dedicated IP Service for your HTTP/HTTPS applications, select "Others" as Application Protocol in Basic Info configuration.|


![null](</docs/resources/images/transports/add-transport-settings-2.png>)

| Fields               | Description   |
| -------------------- | ------------- |
| Carry Client IP      | <strong> NO </strong>: Disable the function. By default, HDT will try to add the X-Forwarded-For header into the request to carry the client’s real IP address for HTTP and HTTPS applications. (For HTTPS applications, the client certificate must be deployed on the HDT servers. Please contact the HDT support team if you need to deploy a client certificate.) <br> <strong> TCP Option 0x4e </strong>: HDT establishes a TCP connection with the origin server and sends the client's real IP address to the origin server through the tcp-option 0x4e in the TCP message; the origin server can obtain the client's real IP address through the F5 device or the Linux kernel module provided by HDT. <br> <strong>proxy protocol v1</strong>: By using proxy protocol v1, HDT establishes a TCP connection with the origin server and sends the client's real IP address to the origin server in the first packet; the origin server obtains the client's real IP address by parsing the proxy protocol v1 message. <br> <strong>proxy protocol v2 </strong>: By using proxy protocol v2, HDT establishes a TCP connection with the origin server and sends the client's real IP address to the origin server in the first packet; the origin server obtains the client's real IP address by parsing the proxy protocol v2 message.|
|Transfer Strategy     | <strong> Default </strong>: Low cost and high efficiency. <br> <strong> Interactive </strong>: For applications requiring better response times, HDT internal routing is enabled in this mode. <br> <strong> High Concurrency </strong>：Suitable for small data transfers and high concurrency. Normally, concurrency is considered to be high when its value exceeds 1,000 connections and low when its value is below 100 connections. <br> <strong> High Real-time </strong>: Suitable for applications delivering small data with low concurrency (fewer than 100 connections) and requiring optimized response times. |

## Security
![null](</docs/resources/images/transports/add-transport-security.png>)

## Review
![null](</docs/resources/images/transports/add-transport-review.png>)

