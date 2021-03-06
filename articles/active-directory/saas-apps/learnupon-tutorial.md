---
title: 'Tutorial: Azure Active Directory integration with LearnUpon | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and LearnUpon.
services: active-directory
documentationCenter: na
author: jeevansd
manager: mtillman
ms.reviewer: barbkess

ms.assetid: b11c6315-c79d-4f34-9610-bd17070ab7c7
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: tutorial
ms.date: 04/14/2019
ms.author: jeedes

ms.collection: M365-identity-device-management
---
# Tutorial: Azure Active Directory integration with LearnUpon

In this tutorial, you learn how to integrate LearnUpon with Azure Active Directory (Azure AD).
Integrating LearnUpon with Azure AD provides you with the following benefits:

* You can control in Azure AD who has access to LearnUpon.
* You can enable your users to be automatically signed-in to LearnUpon (Single Sign-On) with their Azure AD accounts.
* You can manage your accounts in one central location - the Azure portal.

If you want to know more details about SaaS app integration with Azure AD, see [What is application access and single sign-on with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-appssoaccess-whatis).
If you don't have an Azure subscription, [create a free account](https://azure.microsoft.com/free/) before you begin.

## Prerequisites

To configure Azure AD integration with LearnUpon, you need the following items:

* An Azure AD subscription. If you don't have an Azure AD environment, you can get a [free account](https://azure.microsoft.com/free/)
* LearnUpon single sign-on enabled subscription

## Scenario description

In this tutorial, you configure and test Azure AD single sign-on in a test environment.


* LearnUpon supports **IDP** initiated SSO

* LearnUpon supports **Just In Time** user provisioning


## Adding LearnUpon from the gallery

To configure the integration of LearnUpon into Azure AD, you need to add LearnUpon from the gallery to your list of managed SaaS apps.

**To add LearnUpon from the gallery, perform the following steps:**

1. In the **[Azure portal](https://portal.azure.com)**, on the left navigation panel, click **Azure Active Directory** icon.

	![The Azure Active Directory button](common/select-azuread.png)

2. Navigate to **Enterprise Applications** and then select the **All Applications** option.

	![The Enterprise applications blade](common/enterprise-applications.png)

3. To add new application, click **New application** button on the top of dialog.

	![The New application button](common/add-new-app.png)

4. In the search box, type **LearnUpon**, select **LearnUpon** from result panel then click **Add** button to add the application.

	![LearnUpon in the results list](common/search-new-app.png)

## Configure and test Azure AD single sign-on

In this section, you configure and test Azure AD single sign-on with LearnUpon based on a test user called **Britta Simon**.
For single sign-on to work, a link relationship between an Azure AD user and the related user in LearnUpon needs to be established.

To configure and test Azure AD single sign-on with LearnUpon, you need to complete the following building blocks:

1. **[Configure Azure AD Single Sign-On](#configure-azure-ad-single-sign-on)** - to enable your users to use this feature.
2. **[Configure LearnUpon Single Sign-On](#configure-learnupon-single-sign-on)** - to configure the Single Sign-On settings on application side.
3. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with Britta Simon.
4. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable Britta Simon to use Azure AD single sign-on.
5. **[Create LearnUpon test user](#create-learnupon-test-user)** - to have a counterpart of Britta Simon in LearnUpon that is linked to the Azure AD representation of user.
6. **[Test single sign-on](#test-single-sign-on)** - to verify whether the configuration works.

### Configure Azure AD single sign-on

In this section, you enable Azure AD single sign-on in the Azure portal.

To configure Azure AD single sign-on with LearnUpon, perform the following steps:

1. In the [Azure portal](https://portal.azure.com/), on the **LearnUpon** application integration page, select **Single sign-on**.

    ![Configure single sign-on link](common/select-sso.png)

2. On the **Select a Single sign-on method** dialog, select **SAML/WS-Fed** mode to enable single sign-on.

    ![Single sign-on select mode](common/select-saml-option.png)

3. On the **Set up Single Sign-On with SAML** page, click **Edit** icon to open **Basic SAML Configuration** dialog.

	![Edit Basic SAML Configuration](common/edit-urls.png)

4. On the **Basic SAML Configuration** section, perform the following steps:

    ![LearnUpon Domain and URLs single sign-on information](common/idp-reply.png)

    In the **Reply URL** text box, type a URL using the following pattern:
    `https://<companyname>.learnupon.com/saml/consumer`

	> [!NOTE]
	> The value is not real. Update the value with the actual Reply URL. Contact [LearnUpon Client support team](https://www.learnupon.com/features/support/) to get the value. You can also refer to the patterns shown in the **Basic SAML Configuration** section in the Azure portal.

5. On the **Set up Single Sign-On with SAML** page, locate the **THUMBPRINT** - This will be added to your LearnUpon SAML Settings.

	![The Certificate download link](common/certificateraw.png)

6. On the **Set up LearnUpon** section, copy the appropriate URL(s) as per your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

	a. Login URL

	b. Azure AD Identifier

	c. Logout URL

### Configure LearnUpon Single Sign-On

1. Open another browser instance and sign in into LearnUpon with an administrator account.

1. Click the **settings** tab.

    ![Configure Single Sign-On](./media/learnupon-tutorial/tutorial_learnupon_06.png)

1. Click **Single Sign On - SAML**, and then click **General Settings** to configure SAML settings.
   
    ![Configure Single Sign-On](./media/learnupon-tutorial/tutorial_learnupon_07.png) 

1. In the **General Settings** section, perform the following steps:
   
    ![Configure Single Sign-On](./media/learnupon-tutorial/tutorial_learnupon_08.png)  
  
	a. Select **Enabled**.

	b. Select **Version** as **2.0**.

	c. Select **Skip conditions** as **No**.

	d. In the **SAML Token Post param name** textbox, type the name of request post parameter to the SAML consumer URL indicated above that contains the SAML Assertion to be verified and authenticated - for example **SAMLResponse**.

	e. In the **Name Identifier Format** textbox, type the value that indicates where in your SAML Assertion the users identifier (Email address) resides - for example `urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress`.
  
	f. In the **Identify Provider Location** textbox, type the value that indicates where the users are sent to if they click on your uploaded icon from your Azure portal login screen.
  
	g. In the **Sign out URL** textbox, paste the **Logout URL** value, which you have copied from the Azure portal.

	h. Click **Manage finger prints**, and then upload the finger print of your downloaded certificate.

1. Click **User Settings**, and then perform the following steps:

     ![Configure Single Sign-On](./media/learnupon-tutorial/tutorial_learnupon_11.png)  

	a. In the **First Name Identifier Format** textbox, type the value that tells us where in your SAML Assertion the users firstname resides - for example: `http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname`.
  
	b. In the **Last Name Identifier Format** textbox, type the value that tells us where in your SAML Assertion the users lastname resides - for example: `http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname`.

### Create an Azure AD test user

The objective of this section is to create a test user in the Azure portal called Britta Simon.

1. In the Azure portal, in the left pane, select **Azure Active Directory**, select **Users**, and then select **All users**.

    ![The "Users and groups" and "All users" links](common/users.png)

2. Select **New user** at the top of the screen.

    ![New user Button](common/new-user.png)

3. In the User properties, perform the following steps.

    ![The User dialog box](common/user-properties.png)

    a. In the **Name** field enter **BrittaSimon**.
  
    b. In the **User name** field type `brittasimon@yourcompanydomain.extension`. For example, BrittaSimon@contoso.com

    c. Select **Show password** check box, and then write down the value that's displayed in the Password box.

    d. Click **Create**.

### Assign the Azure AD test user

In this section, you enable Britta Simon to use Azure single sign-on by granting access to LearnUpon.

1. In the Azure portal, select **Enterprise Applications**, select **All applications**, then select **LearnUpon**.

	![Enterprise applications blade](common/enterprise-applications.png)

2. In the applications list, select **LearnUpon**.

	![The LearnUpon link in the Applications list](common/all-applications.png)

3. In the menu on the left, select **Users and groups**.

    ![The "Users and groups" link](common/users-groups-blade.png)

4. Click the **Add user** button, then select **Users and groups** in the **Add Assignment** dialog.

    ![The Add Assignment pane](common/add-assign-user.png)

5. In the **Users and groups** dialog select **Britta Simon** in the Users list, then click the **Select** button at the bottom of the screen.

6. If you are expecting any role value in the SAML assertion then in the **Select Role** dialog select the appropriate role for the user from the list, then click the **Select** button at the bottom of the screen.

7. In the **Add Assignment** dialog click the **Assign** button.

### Create LearnUpon test user

In this section, a user called Britta Simon is created in LearnUpon. LearnUpon supports just-in-time user provisioning, which is enabled by default. There is no action item for you in this section. If a user doesn't already exist in LearnUpon, a new one is created after authentication. If you need to create an user manually, you need to contact [LearnUpon support team](https://www.learnupon.com/features/support/).

### Test single sign-on

In this section, you test your Azure AD single sign-on configuration using the Access Panel.

When you click the LearnUpon tile in the Access Panel, you should be automatically signed in to the LearnUpon for which you set up SSO. For more information about the Access Panel, see [Introduction to the Access Panel](https://docs.microsoft.com/azure/active-directory/active-directory-saas-access-panel-introduction).

## Additional Resources

- [List of Tutorials on How to Integrate SaaS Apps with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-saas-tutorial-list)

- [What is application access and single sign-on with Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/active-directory-appssoaccess-whatis)

- [What is Conditional Access in Azure Active Directory?](https://docs.microsoft.com/azure/active-directory/conditional-access/overview)