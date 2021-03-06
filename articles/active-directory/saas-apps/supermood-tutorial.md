---
title: 'Tutorial: Azure Active Directory integration with Supermood | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and Supermood.
services: active-directory
documentationCenter: na
author: jeevansd
manager: femila
ms.reviewer: joflore

ms.assetid: afc04efa-2eba-4e47-8ce4-b71eb293cd09
ms.service: active-directory
ms.component: saas-app-tutorial
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 06/12/2018
ms.author: jeedes

---
# Tutorial: Azure Active Directory integration with Supermood

In this tutorial, you learn how to integrate Supermood with Azure Active Directory (Azure AD).

Integrating Supermood with Azure AD provides you with the following benefits:

- You can control in Azure AD who has access to Supermood.
- You can enable your users to automatically get signed-on to Supermood (Single Sign-On) with their Azure AD accounts.
- You can manage your accounts in one central location - the Azure portal.

If you want to know more details about SaaS app integration with Azure AD, see [what is application access and single sign-on with Azure Active Directory](../manage-apps/what-is-single-sign-on.md).

## Prerequisites

To configure Azure AD integration with Supermood, you need the following items:

- An Azure AD subscription
- A Supermood single sign-on enabled subscription

> [!NOTE]
> To test the steps in this tutorial, we do not recommend using a production environment.

To test the steps in this tutorial, you should follow these recommendations:

- Do not use your production environment, unless it is necessary.
- If you don't have an Azure AD trial environment, you can [get a one-month trial](https://azure.microsoft.com/pricing/free-trial/).

## Scenario description
In this tutorial, you test Azure AD single sign-on in a test environment. 
The scenario outlined in this tutorial consists of two main building blocks:

1. Adding Supermood from the gallery
2. Configuring and testing Azure AD single sign-on

## Adding Supermood from the gallery
To configure the integration of Supermood into Azure AD, you need to add Supermood from the gallery to your list of managed SaaS apps.

**To add Supermood from the gallery, perform the following steps:**

1. In the **[Azure portal](https://portal.azure.com)**, on the left navigation panel, click **Azure Active Directory** icon. 

	![The Azure Active Directory button][1]

2. Navigate to **Enterprise applications**. Then go to **All applications**.

	![The Enterprise applications blade][2]
	
3. To add new application, click **New application** button on the top of dialog.

	![The New application button][3]

4. In the search box, type **Supermood**, select **Supermood** from result panel then click **Add** button to add the application.

	![Supermood in the results list](./media/supermood-tutorial/tutorial_supermood_addfromgallery.png)

## Configure and test Azure AD single sign-on

In this section, you configure and test Azure AD single sign-on with Supermood based on a test user called "Britta Simon".

For single sign-on to work, Azure AD needs to know what the counterpart user in Supermood is to a user in Azure AD. In other words, a link relationship between an Azure AD user and the related user in Supermood needs to be established.

To configure and test Azure AD single sign-on with Supermood, you need to complete the following building blocks:

1. **[Configure Azure AD Single Sign-On](#configure-azure-ad-single-sign-on)** - to enable your users to use this feature.
2. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with Britta Simon.
3. **[Create a Supermood test user](#create-a-supermood-test-user)** - to have a counterpart of Britta Simon in Supermood that is linked to the Azure AD representation of user.
4. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable Britta Simon to use Azure AD single sign-on.
5. **[Test single sign-on](#test-single-sign-on)** - to verify whether the configuration works.

### Configure Azure AD single sign-on

In this section, you enable Azure AD single sign-on in the Azure portal and configure single sign-on in your Supermood application.

**To configure Azure AD single sign-on with Supermood, perform the following steps:**

1. In the Azure portal, on the **Supermood** application integration page, click **Single sign-on**.

	![Configure single sign-on link][4]

2. On the **Single sign-on** dialog, select **Mode** as	**SAML-based Sign-on** to enable single sign-on.
 
	![Single sign-on dialog box](./media/supermood-tutorial/tutorial_supermood_samlbase.png)

3. On the **Supermood Domain and URLs** section, perform the following steps:

	![Supermood Domain and URLs single sign-on information](./media/supermood-tutorial/tutorial_supermood_url.png)

	a. Check **Show advanced URL settings**.

    b. If you wish to configure the application in **IDP** initiated mode, in the **Relay State** textbox, type a URL: `https://supermood.co/auth/sso/saml20`

	c. If you wish to configure the application in **SP** initiated mode, in the **Sign-on URL** textbox, type a URL: `https://supermood.co/app/#!/loginv2`

4. Supermood application expects the SAML assertions in a specific format. Configure the following claims for this application. You can manage the values of these attributes from the **User Attributes** section on application integration page. The following screenshot shows an example for this.
	
	![Configure Single Sign-On](./media/supermood-tutorial/tutorial_supermood_attribute.png)

5. In the **User Attributes** section on the **Single sign-on** dialog, configure SAML token attribute as shown in the image above and perform the following steps:
    
	| Attribute Name | Attribute Value |
	| ---------------| --------------- |    
	| firstName | user.givenname |
	| lastName | user.surname |

	a. Click **Add attribute** to open the **Add Attribute** dialog.

	![Configure Single Sign-On](./media/supermood-tutorial/tutorial_attribute_04.png)

	![Configure Single Sign-On](./media/supermood-tutorial/tutorial_attribute_05.png)
	
	b. In the **Name** textbox, type the attribute name shown for that row.
	
	c. From the **Value** list, type the attribute value shown for that row.

	d. Leave the **Namespace** blank.
	
	d. Click **Ok**

6. On the **SAML Signing Certificate** section, click the copy button to copy **App Federation Metadata Url** and paste it into notepad.

	![The Certificate download link](./media/supermood-tutorial/tutorial_supermood_certificate.png) 

7. Click **Save** button.

	![Configure Single Sign-On Save button](./media/supermood-tutorial/tutorial_general_400.png)

8. Go to your Supermood.co admin panel as Security Administrator.

9. Click on **My account** (bottom left) and **Single Sign On (SSO)**.

	![The Certificate single](./media/supermood-tutorial/tutorial_supermood_single.png)
10. On **Your SAML 2.0 configurations**, Click **Add an SAML 2.0 configuration for an email domain**.

	![The Certificate add](./media/supermood-tutorial/tutorial_supermood_add.png)

11. On **Add an SAML 2.0 configuration for an email domain**. section, perform the following steps:

	![The Certificate saml](./media/supermood-tutorial/tutorial_supermood_saml.png)

	a. In the **email domain for this Identity provider** textbox, type your domain.

	b. In the **Use a metadata URL** textbox, paste the **App Federation Metadata Url** which you have copied from Azure portal.

	c. Click **Add**.

### Create an Azure AD test user

The objective of this section is to create a test user in the Azure portal called Britta Simon.

   ![Create an Azure AD test user][100]

**To create a test user in Azure AD, perform the following steps:**

1. In the Azure portal, in the left pane, click the **Azure Active Directory** button.

    ![The Azure Active Directory button](./media/supermood-tutorial/create_aaduser_01.png)

2. To display the list of users, go to **Users and groups**, and then click **All users**.

    ![The "Users and groups" and "All users" links](./media/supermood-tutorial/create_aaduser_02.png)

3. To open the **User** dialog box, click **Add** at the top of the **All Users** dialog box.

    ![The Add button](./media/supermood-tutorial/create_aaduser_03.png)

4. In the **User** dialog box, perform the following steps:

    ![The User dialog box](./media/supermood-tutorial/create_aaduser_04.png)

    a. In the **Name** box, type **BrittaSimon**.

    b. In the **User name** box, type the email address of user Britta Simon.

    c. Select the **Show Password** check box, and then write down the value that's displayed in the **Password** box.

    d. Click **Create**.
 
### Create a Supermood test user

In this section, you create a user called Britta Simon in Supermood. Supermood supports just-in-time provisioning, which is by default enabled for users whose emails belong to the domains which are added during the configuration at Supermood end. There is no action item for you in this section. A new user is created during an attempt to access Supermood if it doesn't exist yet.

>[!Note]
>If you need to create a user manually, contact [Supermood support team](mailto:hello@supermood.fr).


### Assign the Azure AD test user

In this section, you enable Britta Simon to use Azure single sign-on by granting access to Supermood.

![Assign the user role][200] 

**To assign Britta Simon to Supermood, perform the following steps:**

1. In the Azure portal, open the applications view, and then navigate to the directory view and go to **Enterprise applications** then click **All applications**.

	![Assign User][201] 

2. In the applications list, select **Supermood**.

	![The Supermood link in the Applications list](./media/supermood-tutorial/tutorial_supermood_app.png)  

3. In the menu on the left, click **Users and groups**.

	![The "Users and groups" link][202]

4. Click **Add** button. Then select **Users and groups** on **Add Assignment** dialog.

	![The Add Assignment pane][203]

5. On **Users and groups** dialog, select **Britta Simon** in the Users list.

6. Click **Select** button on **Users and groups** dialog.

7. Click **Assign** button on **Add Assignment** dialog.
	
### Test single sign-on

In this section, you test your Azure AD single sign-on configuration using the Access Panel.

When you click the Supermood tile in the Access Panel, you should get automatically signed-on to your Supermood application.
For more information about the Access Panel, see [Introduction to the Access Panel](../active-directory-saas-access-panel-introduction.md). 

## Additional resources

* [List of Tutorials on How to Integrate SaaS Apps with Azure Active Directory](tutorial-list.md)
* [What is application access and single sign-on with Azure Active Directory?](../manage-apps/what-is-single-sign-on.md)



<!--Image references-->

[1]: ./media/supermood-tutorial/tutorial_general_01.png
[2]: ./media/supermood-tutorial/tutorial_general_02.png
[3]: ./media/supermood-tutorial/tutorial_general_03.png
[4]: ./media/supermood-tutorial/tutorial_general_04.png

[100]: ./media/supermood-tutorial/tutorial_general_100.png

[200]: ./media/supermood-tutorial/tutorial_general_200.png
[201]: ./media/supermood-tutorial/tutorial_general_201.png
[202]: ./media/supermood-tutorial/tutorial_general_202.png
[203]: ./media/supermood-tutorial/tutorial_general_203.png

