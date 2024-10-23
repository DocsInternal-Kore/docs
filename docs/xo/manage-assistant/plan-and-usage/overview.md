
# Plan and Usage Overview
  
This article provides information on how Apps are billed, how to track their usage and the usage limits or quotas applied for various features. Before we go into the details, let's quickly understand the following key terms and concepts.

## Accounts or Workspaces

A Workspace or Account refers to a group of users who typically belong to an organization or work on projects. When you sign up, the platform automatically creates a Workspace and a User identity. In some scenarios, the platform creates only a user identity and associates you with an existing Workspace. To learn how workspaces are created for different usage scenarios, see [Accessing the Platform](../../getting-started/accessing-the-platform.md)

## Workspace Owner

The workspace or account owner is the user who has created the workspace. Workspace Owner has access to the Administration Console and the Manage Workspace feature. This user can invite additional users to the workspace, manage their roles, and view the plan and usage details of the apps in the workspace.

## App Owner

The user who creates an app becomes its owner by default. The owner can invite other users to the app for collaboration. The owner can transfer the ownership to another user of the workspace. Workspace Owner can also change the ownership from the Administration Console. A user can create more than one app and own all of them.

## Collaborators

The workspace or app owner can invite other users to collaborate on an app. Collaborators/co-developers/shared developers have limited access to the app based on their assigned roles. A user can be a collaborator on some apps and an owner on others.

## Workspace Types

Every workspace of the Kore.ai XO Platform is categorized as a Standard or Enterprise workspace. The licenses, usage, and limits of the apps developed using the Kore.ai XO Platform are governed by Kore.ai’s terms and conditions associated with your workspace.

### Standard Workspace

Every workspace gets classified as a Standard Workspace when created. All the apps published in the Standard Workspace are auto-assigned with the Standard Usage Plan.

* Standard Workspaces get free credits worth $500. The free credits are valid for 90 days from the date of workspace creation. They can be used to publish and test the app. You can continue to build your apps even after the free credits have expired or been exhausted. However, the apps will stop responding on the channels after the free credits are exhausted or expired.
* Standard Workspaces provides a pay-as-you-go model for deploying the app for production purposes.
* Workspace or App Owners can request to upgrade to Enterprise Workspace. Kore.ai’s Customer Support team will contact the users to process the request.

### Enterprise Workspace

Enterprise workspaces offer access to premium features, higher usage limits, and rate limits. The workspaces of business accounts that have custom contracts with Kore.ai are auto-upgraded to Enterprise Workspaces.

* The features, usage limits, and rate limits for the Enterprise workspaces are governed by the terms and conditions of the license agreement.
* All the apps in the Enterprise Workspace are assigned to the Enterprise Usage Plan. For more information, see [Usage Plans](../plan-and-usage/usage-plans.md).

#### Upgrade Flow for Enterprise Workspace

**Specific Product Upgrades**  
When upgrading to an enterprise workspace, the upgrade applies only to specific products. For example, if a customer purchases only Search AI, the workspace will be upgraded only for the Search AI license. Access to other products is not granted.
Refer to the below image for an upgrade from the internal tool.

<img src="../images/manage-workspace.png" alt="Manage Workspace" title="Manage Workspace" style="border:1px solid gray;zoom:60%;">


**Post-Upgrade Access**

Once the upgrade is completed, users gain immediate access to the eligible products without needing to go through the trial flow again. For example, Automation and Contact Center AI show the **Try Now** buttons before the upgrade. After the upgrade, they are shown as **Create New**. Similarly, the **Contact Us** buttons are replaced with **Create New** for Search AI and Agent AI.

<img src="../images/post-upgrade-access.png" alt="Post-Upgrade Access" title="Post-Upgrade Access" style="border:1px solid gray;zoom:60%;">


Inside an app, users can access all the products for which the enterprise has licenses.

<img src="../images/product switcher.png" alt="product" title="product" style="border:1px solid gray;zoom:60%;">

**Enterprise Upgrade for Fewer Products**

* The internal tool allows for assigning enterprise licenses to specific products only.
* In the scenarios where only certain products are upgraded to enterprise, users can create apps using only those for which enterprise licenses are provided.
In the below example, only Automation AI and SearchAI enterprise licenses are offered. Contact Center and Agent licenses are not included.

<img src="../images/get-started.png" alt="Get Started" title="Get Started" style="border:1px solid gray;zoom:60%;">

## Plan Types

The Kore.ai XO Platform offers Usage Plans for deploying and managing your App.

### Usage Plans

The Usage Plan enables apps to interact with your end users from any available channels.  channels. For more information, see [Usage Plans](../plan-and-usage/usage-plans.md).

## Workspace Linked to Multiple Apps

A workspcae owner can explicitly manage the Plan and Usage for a workspace linked to multiple bot accounts and do the following:

* Manage the free and paid credits for individual bots listed for a standard account.
* View the number of paid and inactive bots.
* View free credit statistics.
* Upgrade the current plan.
* Add funds to the existing plan.
* View **Current Credits**, **Allowed Requests**, and **Usage Trends** for the current plan.
* View the **Billing Request Trend** across weeks, months, or custom date ranges.
* View the **Support Plan Type**, **Subscription Type** (monthly/yearly), **Subscription Fee**, and **Renewal Due Date** values.
* Access the **Manage Tickets** and **Community** pages.


