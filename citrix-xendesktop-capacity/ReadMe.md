<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https://raw.githubusercontent.com/brianehlert/azure-quickstart-templates/myUI/citrix-xendesktop-capacity/azuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https://raw.githubusercontent.com/brianehlert/azure-quickstart-templates/myUI/citrix-xendesktop-capacity/azuredeploy.json" target="_blank">
  <img src="http://armviz.io/visualizebutton.png"/>
</a>

This template creates resource groups and assigns minimum permissions to an application service principal account for creating and managing workstations and the required Citrix infrastrucutre:

The following Resource Groups will be created:
- Citrix Infrastructure
- Citrix Image Store
- Citrix Workstations

The selected application service principal will be assigned rights to the subscription (Dedicated) or rights to individual resource groups (delegated).

The selected service principal will be granted read only access to the image store, and to the selected Virtual Network.

Prior to running this template, please ensure that you have established the following:
- Virtual Network and subnet(s) for use by the workstations and Citrix infrastrucutre machines.
- Azure Active Directory with either Azure Active Directory Domain Services or a replica Domain Controller instance attached to the above virtual network.
- Update the DNS settings of the virtual network to the AADDS or AD machine instance(s) IP addresses.
- Create a subscription for your Citrix XenDekstop Express deployment (Citrix recommends creating subscription(s) for XenDestkop Express that are seperate from other corporate infrastructure)
- Application Service Principal for use by the Citrix Cloud Service to access your XenDesktop Express machines and to manage workstation lifecycle.  If not, you can run this <> template

