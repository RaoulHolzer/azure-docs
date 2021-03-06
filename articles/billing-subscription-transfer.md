---
title: Transferring ownership of an Azure subscription| Microsoft Docs
description: How to transfer an Azure subscription to another user, and some frequently asked questions (FAQ) about the process
services: ''
documentationcenter: ''
author: genlin
manager: stevenpo
editor: ''
tags: billing,top-support-issue

ms.assetid: c8ecdc1e-c9c5-468c-a024-94ae41e64702
ms.service: billing
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 12/8/2016
ms.author: genli

---
# Transferring ownership of an Azure subscription

You can easily transfer your subscription to another user for Pay-As-You-Go, MSDN, Action Pack, or BizSpark subscriptions. You can change the account administrator on any Pay-As-You-Go, MSDN, Action Pack, or BizSpark subscription that you own, no matter which country you operate in. We support the transfer of Azure Marketplace Purchases for these subscription types as well. 

You might want to transfer ownership of an Azure subscription if you:

* Need to hand over billing ownership of your Azure subscription to someone else.
* Want to change the account used to sign up for Azure. Perhaps you used your Microsoft Account but meant to use your work or school account instead.
* Want to move your Azure subscription from one directory to another.
* Have Azure and Office 365 in different tenants and want to consolidate.

To change your subscription to a different offer, see [Switch your Azure subscription to another offer](billing-how-to-switch-azure-offer.md). 

## How to transfer ownership of an Azure subscription
> [!VIDEO https://channel9.msdn.com/Series/Microsoft-Azure-Tutorials/Transfer-an-Azure-subscription/player]
>
>

1. Sign in at <https://account.windowsazure.com/Subscriptions>. You have to be the account administrator to perform an ownership transfer. For more information about how to find out who is the account administrator of the subscription, see the [Frequently asked questions](#faq).
2. Select the subscription to transfer.
3. Click the **Transfer Subscription** option.

   ![Azure account subscriptions tab](./media/billing-subscription-transfer/image1.png)
4. Follow the prompts to specify the recipient.

   ![Transfer Subscription dialog box](./media/billing-subscription-transfer/image2.PNG)
5. The recipient automatically gets an email with an acceptance link.

   ![Subscription transfer email to recipient](./media/billing-subscription-transfer/image3.png)
6. The recipient clicks the link and follows the instructions,
   including entering their payment information.

   ![First subscription transfer web page](./media/billing-subscription-transfer/image4.png)

   ![Second subscription transfer web page](./media/billing-subscription-transfer/image5.png)
7. Success! The subscription is now transferred.

<a id="faq"></a>

## Frequently asked questions (FAQ)
* <a name="whoisaa"></a> **Who is the account administrator of the subscription?**

  The account administrator is the person who signed up for or bought the Azure subscription. They're authorized to access the [Account Center](https://account.windowsazure.com/Home/Index) and perform various management tasks like create subscriptions, cancel subscriptions, change the billing for a subscription, or change the Service Administrator. If you're not sure who the account administrator is for a subscription, use the following steps to find out.

  1. Sign in to the [Azure portal](https://portal.azure.com).
  2. On the Hub menu, select **Subscription**.
  3. Select the subscription you want to check, and then look under **Settings**.
  4. Select **Properties**. The account administrator of the subscription is displayed in the **Account Admin** box.  
* **Does a subscription transfer result in any service downtime?**

  There is no impact to the service. Transferring the subscription cancels the
  subscription under the current Account Administrator and creates a subscription under the recipient’s account. The new subscription is associated to the underlying Azure services. The subscription ID remains the same.
* **How do I use this process to change the directory for subscription?**   
  An Azure subscription is created in the directory that the Account Administrator belongs to. To change the directory, transfer the subscription to a user account in the target directory. When that user completes the steps to accept transfer, the subscription is automatically moved to the target directory.
* **If I take over billing ownership of a subscription from another
  organization, do they continue to have access to my resources?**

  If the subscription is transferred to another tenant, the users associated with the previous tenant lose access to the subscription. Even if a user is not a Service Admin or Co-admin anymore, they might still have access to the subscription through other security mechanisms. These include:

  * Management certificates that grant the user admin rights to subscription resources. For more information, see [Create and Upload a Management Certificate for Azure](https://msdn.microsoft.com/library/azure/gg551722.aspx)
  * Access keys for services like Storage. For more information, see [About Azure storage accounts](storage/storage-create-storage-account.md)
  * Remote Access credentials for services like Azure Virtual Machines

  This is not a complete list. The recipient should consider updating any secrets associated with the service if they need to restrict access to their resources. Most resources can be updated as follows:

  1. Go to the [Azure portal](https://portal.azure.com).
  2. On the Hub menu, select **All resources**.
  3. Select the resource. 
  4. In the resource blade, click **Settings**. Here you can view and update existing secrets.
* **If I transfer the subscription in the middle of the billing cycle,
  does the recipient pay for the entire billing cycle?**

  The sender is responsible for payment for any usage that was reported up to the point that the transfer is completed. The recipient is responsible for usage reported from the time of
  transfer onwards. There may be some usage that took place before transfer but was reported afterwards. The usage is included in the recipient’s bill.
* **Does the recipient have access to usage and billing history?**

  The only information available to the recipient is the amount of the last bill or if the subscription was transferred before the first bill was generated, the current balance. The rest of the usage and billing history does not transfer with the subscription.
* **Can the offer be changed during a transfer?**

  The offer must remain the same. To change your offer, you must [contact Support](http://go.microsoft.com/fwlink/?LinkID=619338).
* **Can I transfer a subscription to a user account in another
  country?**

  No, transferring a subscription to a user account in another country is not supported. The recipient’s user account must be in the same country.
* **Can the recipient use a different payment method?**

  Yes. But the subscription billing history is split across two accounts.  

* **Is the payment method impacted after I transferred an Azure subscription?**

To accept a subscription transfer, a credit card, or similar payment method must be provided to pay for the subscription. For example, if Bob transfers a subscription to Jane and Jane accepts the transfer, Jane must also provide a payment method that she used to pay for the subscription. After the transfer is complete, Bob is no longer charged for the subscription he transferred to Jane.

* **How do I migrate data and services for my Azure subscription to new subscription?**

  See [Move resources to new resource group or subscription](./azure-resource-manager/resource-group-move-resources.md).

## Next steps after accepting ownership of a subscription
1. You are now the Account Administrator. Review and update the Service Administrator and Co-Administrators. Manage admins in the [Azure classic portal](https://manage.windowsazure.com) by going to Settings. [Learn more](http://go.microsoft.com/fwlink/?LinkID=533293).
2. You can also use role-based access control (RBAC) for your subscription and services. Visit the [Azure portal](https://portal.azure.com) [Learn more about RBAC](http://go.microsoft.com/fwlink/?LinkID=544802)
3. Update credentials associated with this subscription's services. These include:
   * Management certificates that grant the user admin rights to subscription resources. For more information, see [Create and upload a management certificate for Azure](https://msdn.microsoft.com/library/azure/gg551722.aspx)
   * Access keys for services like Storage. For more information, see [About Azure storage accounts](storage/storage-create-storage-account.md)
   * Remote Access credentials for services like Azure Virtual Machines
4. Update billing alerts for this subscription, at the [Azure Account Center](https://account.windowsazure.com/Subscriptions). [Learn more](http://go.microsoft.com/fwlink/?LinkID=533292)
5. If you’re working with a partner, consider updating the partner ID on this subscription. You can update the partner ID in the [Azure Account Center](https://account.windowsazure.com/Subscriptions).


## Need help? Contact support.
If you still need help, [contact support](https://portal.azure.com/?#blade/Microsoft_Azure_Support/HelpAndSupportBlade) to get your issue resolved quickly. 


