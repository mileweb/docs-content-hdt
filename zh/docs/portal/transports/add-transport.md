# 新增加速项
1. 点击左侧导航界面中的**加速项**进入加速项页面。
2. 在加速项页面的右上角点击**+ 新增加速项** 按钮进入加速项配置页面。 
3. 填写基本信息, 标注(\*)的为必填项。完成后点击右上角的**\>下一步**。

![null](</docs/resources/images/transports/add-transport-basic-info.png>)

4. 填写设置页面信息，标注(\*)的为必填项。完成后点击右上角的**\>下一步**。

![null](</docs/resources/images/transports/add-transport-settings.png>)

| 选项                 | 描述          |
| -------------------- | ------------- |
| 固定接出             | 如果您选择了“是”, HDT接出服务器 (HDT连接源站的服务器) 将固定使用您所选区域的服务器, 加速项创建成功后, 您可以查看接出服务器IP列表。 |

5. 填写安全页面信息，标注(\*)的为必填项。完成后点击右上角的**\>下一步**。

![null](</docs/resources/images/transports/add-transport-security.png>)

6. 在预览页面查看您所录入的加速项配置信息。如果您需要修改一些内容，可以点击之前步骤的图标回到前面的页面进行修改。完成后点击**\>下一步**按钮或直接点击预览步骤图标回到预览页面。确认无误后点击**提交**按钮。

![null](</docs/resources/images/transports/add-transport-review.png>)

# 接入HDT平台
加速项成功创建后，在您的DNS配置中加入一个CNAME记录将您企业应用的服务域名指向新生成的HDT CNAME。
