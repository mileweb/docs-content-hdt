# Add New Transport

The <strong> Transports </strong> page can be reached by clicking "Transports" from the left pane of HDT portal.
To add a new transport, click the **Add New Transport** button at the top-right of the <strong> Transports </strong> page to display the wizard instructions.

## Basic Info
![null](</docs/resources/images/transports/add-transport-basic-info.png>)

| Fields               | Description   |
| -------------------- | ------------- |
| Transport Name       | Enter a name to identify this transport. If you omit this parameter, the HDT portal will generate a default name in the format of "Target Domain:Target Port|
| Version Number       | Version number of the transport configuration in history. |
| Application Protocol | <li><strong> HTTP </strong>: For HTTP protocol.</li> <li><strong> HTTPS </strong>: For HTTPS protocol with SNI(Server Name Indication). |
| IP Version           | IP version of your application supports. |

## Settings
![null](</docs/resources/images/transports/add-transport-settings-1.png>)
![null](</docs/resources/images/transports/add-transport-settings-2.png>)

| Fields               | Description   |
| -------------------- | ------------- |
| Fixed Shields        | The shield servers (the HDT servers that connection to your origin servers) will be fixed. |
| Dedicated IP Service | The IP addresses for serving the transport will be dedicated, and only for the cname. The option will NOT be applicable if you select HTTP or HTTPs as the Application Protocol. To use <strong> Dedicated IP Service </strong> for your HTTP/HTTPs applications, select Others as the Application Protocol.|


![null](</docs/resources/images/transports/add-transport-settings-3.png>)

| Fields               | Description   |
| -------------------- | ------------- |
| Carry Client IP      | <li><strong> NO </strong>: Disable the function. By default, HDT will try to add the X-Forwarded-For header into the request to carry the client’s real IP address for HTTP and HTTPs application. (For HTTPs applications, the client certificate must be deployed at the HDT servers. Please contact HDT support team if you need to deploy a client certificate.) </li> <li><strong> TCP Option 0x4e </strong>: HDT establishes a TCP connection with the origin server and sends the client's real IP address to the origin server through the tcp-option 0x4e in the TCP message; the origin server can obtain the client's real IP address through the F5 device or the Linux kernel module provided by HDT.</li> <li><strong>proxy protocol v1</strong>: Using proxy protocol v1, HDT establishes a TCP connection with the origin server, and sends the client's real IP address to the origin server in the first packet; the origin server obtains the client's real IP address by parsing the proxy protocol v1 message.</li><li><strong>proxy protocol v2 </strong>: Using proxy protocol v2, HDT establishes a TCP connection with the origin server, and sends the client's real IP address to the origin server in the first packet; the origin server obtains the client's real IP address by parsing the proxy protocol v2 message.</li>|
|Transfer Strategy     |<li><strong> Default </strong>: Low cost and high efficiency. </li> <li><strong> Interactive </strong>: For applications requiring better response time, HDT internal routing is enabled in this mode. </li> <li><strong> High Concurrency </strong>：Suitable for small data transfers and high concurrency. Normally, concurrency is considered to be high when its value exceeds 1,000 connections and low when its value is below than 100 connections. </li> <li><strong> High Real-time </strong>: Suitable for applications that deliver small data with low concurrency (fewer than 100 connections) and require optimized response time. </li> |

## Security
![null](</docs/resources/images/transports/add-transport-security.png>)

## Review
![null](</docs/resources/images/transports/add-transport-review.png>)

