# Add New Transport
1. In the left pane of the HDT portal, click **Transports**.
2. At the top right of the Transports page, click the **+ Add New Transport** button. 
3. Fill in the fields of the Basic Info configurations. Required fields are denoted by an asterisk (\*). When completed, click **\> Next** at the top right of the wizard.

![null](</docs/resources/images/transports/add-transport-basic-info.png>)

4. Fill in the fields of the Settings configurations. Required fields are denoted by an asterisk (\*). When completed, click **\> Next** at the top right of the wizard.

![null](</docs/resources/images/transports/add-transport-settings-1.png>)

| Fields               | Description   |
| -------------------- | ------------- |
| Fixed Shields        | If you select Yes, the shield servers (HDT servers that connect to your origin servers) will be static, and you need to choose the region of shield servers in the drop-down list. |

![null](</docs/resources/images/transports/add-transport-settings-2.png>)

| Fields                       | Description   |
| ---------------------------- | ------------- |
| Preserve Client IP Addresses | **NO**: Disable the function.<br>**TCP Option 0x4e**: By using TCP Option 0x4e in TCP messages, HDT sends the client's real IP address to the origin server.<br>**Proxy Protocol v1**: By using Proxy Protocol v1, HDT sends the client's real IP address to the origin server in the first packet.<br>**proxy protocol v2**: By using Proxy Protocol v2, HDT sends the client's real IP address to the origin server in the first packet.|
| Transfer Strategy            | **Default**: For most of applications.<br>**High Real-time**: For applications deliver small data with low concurrency (<100 connections).<br>**Big-File**: For applications transfer big files (>100M).<br>**High Concurrency**：For applications with high concurrency (>1000 connections).<br>**Interactive**: For applications with interactive scenarios.|

5. Fill in the fields of the Security configurations. When completed, click **\> Next** at the top right of the wizard.
![null](</docs/resources/images/transports/add-transport-security.png>)

6. Review your inputs from the previous steps. If you need to change them, click **Previous** to return to the appropriate step, make your changes, and then click **Next** until you return to the Review step.
![null](</docs/resources/images/transports/add-transport-review.png>)

10. When you are satisfied with your inputs, click **Save**.

After the transport is successfully created, add a CNAME record on your DNS server to point your service hostname(s) to the newly created HDT CNAME.
