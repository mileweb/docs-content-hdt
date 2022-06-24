# Add New Transport
1. In the left pane of the HDT portal, click **Transports**.
2. At the top-right of the Transports page, click the **+ Add New Transport** button. 
3. Fill in the fields of the Basic Info configurations. Required fields are denoted by an asterisk (\*). When completed, click **\> Next** at the top-right of the wizard.

![null](</docs/resources/images/transports/add-transport-basic-info.png>)

4. Fill in the fields of the Settings configurations. Required fields are denoted by an asterisk (\*). When completed, click **\> Next** at the top-right of the wizard.

![null](</docs/resources/images/transports/add-transport-settings.png>)

| Fields               | Description   |
| -------------------- | ------------- |
| Fixed Shields        | If you select "Yes", the shield servers (HDT servers that connect to your origin servers) will be only from the region you select, and you can view the shield servers IP list after the transport is successfully created. |

5. Fill in the fields of the Security configurations. When completed, click **\> Next** at the top-right of the wizard.
![null](</docs/resources/images/transports/add-transport-security.png>)

6. Review your inputs from the previous steps. If you need to change them, click **Previous** to return to the appropriate step, make your changes, and then click **Next** until you return to the Review step.
![null](</docs/resources/images/transports/add-transport-review.png>)

7. When you are satisfied with your inputs, click **Save**.

# Direct the Traffic to HDT platform
After the transport is successfully created, add a CNAME record on your DNS server to point your service hostname(s) to the newly created HDT CNAME.
