
  # DEPLOY AN ENVIRONMENT USING INFRASTRUCTURE AS CODE
  
 ##  Management Tools: CloudFormation
  
 ###  3.1 Deploy the Lab Infrastructure
To deploy the lab infrastructure:

1. Download the CloudFormation script for this lab through this link.
2. Use your administrator account to access the CloudFormation console at https://console.aws.amazon.com/cloudformation/.
3. Choose Create Stack.
4. On the Select Template page, select Upload a template file and select the OE_Inventory_and_Patch_Mgmt.json file you just downloaded.
  
#### AWS CloudFormation Designer

AWS CloudFormation Designer is a graphic tool for creating, viewing, and modifying AWS CloudFormation templates. With Designer you can diagram your template resources using a drag-and-drop interface. You can edit their details using the integrated JSON and YAML editor. AWS CloudFormation Designer can help you see the relationship between template resources.

5. On the Select Template page, in the lower-right corner, click the View in Designer button.
6. Briefly review the graphical representation of the environment we are about to create, including the template in the JSON and YAML formats. You can use this feature to convert between JSON and YAML formats.
7. Choose the Create Stack icon (a cloud with an arrow) to return to the Select Template page.
8. On the Select Template page, choose Next.
  
A CloudFormation template is a JSON or YAML formatted text file that describes your AWS infrastructure containing both optional and required sections. In the next steps, we will provide a name for our stack and parameters that will be passed into the template to help define the resources that will be implemented.

9. In the Specify Details section, define a Stack name, such as OELabStack1.
10. In the Parameters section:
    1.Leave InstanceProfile blank as we have not yet defined an instance profile.
    2. Leave InstanceTypeApp and InstanceTypeWeb as the default free-tier-eligible t2.micro value.
    3. Select the EC2 KeyName you defined earlier from the list.
      - In a browser window, go to https://checkip.amazonaws.com/ to get your IP. Enter your IP address in SSHLocation in CIDR notation (i.e., ending in /32).
      - Define the Workload Name as Test.
      - Choose Next.
11. On the Options page under Tags, define a Key of Owner, with Value set to the username you choose for your administrator. You may define additional keys as needed. The CloudFormation template creates all the example tags given in the discussion on tagging above.
12. Leave all other sections unmodified. Scroll to the bottom of the page and choose Next.
13. On the Review page, review your choices and then choose Create.
14. On the CloudFormation console page
    1. Check the box next to your Stack Name to see its details.
    2. If your Stack Name is not displayed, click the refresh button (circular arrow) in the top right until it appears.
    3. If the details are not displayed, choose the refresh button until details appear.
15. Choose the Events tab for your selected workload to see the activity log from the creation of your CloudFormation stack.
  
When the Status of your stack displays CREATE_COMPLETE in the filter list, you have just created a representation of a typical lift and shift 2-tier application migrated to the cloud.

16. Navigate to the EC2 console to view the deployed systems:
    1. Choose Instances.
    2. Select a server and review the details under its Description and Tag tabs.
    3. (Optional) choose Security Groups and select the Security Group whose name begins with the name of your stack. Examine the inbound rules.
    4. (Optional) navigate to the VPC console and examine the configuration of the VPC you just created.

![stack](https://github.com/aissatoubarry938/Inventory-and-Patch-Management/assets/115582067/00590805-eee7-44ec-9a96-50fcc6c39952)
  
![create_complete](https://github.com/aissatoubarry938/Inventory-and-Patch-Management/assets/115582067/4a991a9c-e707-44f8-8919-c9023c50b45e)
  
![Tags_2](https://github.com/aissatoubarry938/Inventory-and-Patch-Management/assets/115582067/4c8730e4-1c5a-40dc-a03c-c5f726d46efb)

 ![optional_3](https://github.com/aissatoubarry938/Inventory-and-Patch-Management/assets/115582067/34dc86cf-7be2-41f1-94ee-b3da00f0cc4b)

 ![Optional_4](https://github.com/aissatoubarry938/Inventory-and-Patch-Management/assets/115582067/7d64a27d-9240-4648-ba54-2feca4a5193a)
