# Add Transport

To create a transport for your High-speed Data Transmission service select **Transports** from the left pane of HDT portal,  and click **Add New Transport** button at the top right of the **Transports** page. Then the wizard instructions appears.

## Basic Info
![null](</docs/resources/images/transports/add-transport-basic-info.png>)

| Fields               | Description   |
| -------------------- | ------------- |
| Transport Name       | Enter a name that helps you identify this transport, if leave it empty, portal will generate the name as "Target Domain:Target Port" |
| Version Number       | The version number of the transport configuration in the history. |
| Application Protocol | <li><strong> HTTP </strong> : For HTTP protocol.</li> <li><strong> HTTPs </strong> : For HTTPs protocol with SNI(Server Name Indication), if SNI is not supported for the transport, please use <strong> Others </strong>.</li>   <li><strong> FTP </strong> : For FTP protocol.</li> <li><strong> Others </strong> : For other protocols.</li> |

## Settings
![null](</docs/resources/images/transports/add-transport-settings-1.png>)
![null](</docs/resources/images/transports/add-transport-settings-2.png>)

| Fields               | Description   |
| -------------------- | ------------- |
| Fixed Shields        | The shield servers (the HDT servers that connection to your origin servers) will be fixed. |
| Dedicated IP Service | The IPs for serving the transport will be dedicated, and only for the cname. The option will be NOT applicable if you select HTTP or HTTPs as the Application Protocol. If you wish to use <strong> Dedicated IP Service </strong> for your HTTP/HTTPs applications, please select Others as the Application Protocol.|


![null](</docs/resources/images/transports/add-transport-settings-3.png>)

| Fields               | Description   |
| -------------------- | ------------- |
| carry client ip      | <li><strong> NO </strong>：Disable the function. By default, HDT will try to add the X-Forwarded-For header into the request to carry the client’s real IP for HTTP and HTTPs applicaiton. (for HTTPs applications, the client certificate needs to be deployed at the HDT servers beforehand, about how to deploy client certificate, please contact HDT team. )  <br> </li> <li><strong> TCP Option 0x4e </strong>: HDT establishes a TCP connection with the origin server, and sends the client's real IP to the origin server through the tcp-option 0x4e in the TCP message; the origin server can obtain the client's real IP through the F5 device or the linux kernel module provided by HDT.</li> <li><strong>proxy protocol v1 </strong>: Using proxy protocol v1, HDT establishes a TCP connection with the origin server, and sends the client's real IP to the origin server in the first packet; the origin server obtains the client's real IP by parsing the proxy protocol v1 message.</li><li><strong>proxy protocol v2 </strong>: Using proxy protocol v2, HDT establishes a TCP connection with the origin server, and sends the client's real IP to the origin server in the first packet; the origin server obtains the client's real IP by parsing the proxy protocol v2 message.</li>|
|Transfer Strategy     |<li><strong> Default </strong>： Low cost and high efficiency. </li> <li><strong> Interactive </strong>：For applications requiring better response time, HDT internal routing would be enabled in this mode. </li> <li><strong> High Concurrency </strong>：Suitable for small data and high concurrency. Normally we consider the concurrency is high when its value is higher than 1000, it’s low when its value is lower than 100. </li> <li><strong> High Real-time </strong>：Suitable for applications which deliver small data with low concurrency（fewer than 100） and requiring  optimized response time. </li> |

## Security
![null](</docs/resources/images/transports/add-transport-security.png>)

## Review
![null](</docs/resources/images/transports/add-transport-review.png>)

