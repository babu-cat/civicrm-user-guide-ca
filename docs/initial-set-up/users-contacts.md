# How are Drupal or Joomla Users Linked to CiviCRM Contact Records

Every CiviCRM instance sits within a "User Framework" — a [CMS (Backdrop, Drupal, Joomla or WordPress)](../appendices/glossary.md#cms-content-management-system) that handles user authentication (logging in) and gives users various levels of access to CiviCRM features (permissions).

[Contacts](../organising-your-data/contacts.md) are the individuals, organizations and households in CiviCRM. Users, on the other hand, are defined in this context as people who have a username and password to log into CiviCRM via the User Framework/CMS. You probably won't have a User account for every Contact in your CiviCRM instance.

## Drupal behavior:

Whenever a new user **registers** , CiviCRM checks for an existing contact with the same email address.

* If a match is found, the new user is **linked** to the existing CiviCRM contact.
* If no match is found, a new CiviCRM contact is created with the new user's primary email address.

Whenever an existing user **logs in** , CiviCRM checks for a linked contact record. If none exists, the same logic applies - either link the user to an existing contact or create a new contact. This case applies when CiviCRM is installed or enabled for an existing Drupal site. However, we recommend that you run the batch synchronization utility (next section) in this situation.

## Joomla behavior:

CiviCRM does not natively use the hooks and APIs of Joomla to facilitate hooking into the user registration and login pages. As a result, in com_user neither a new user registration nor an existing user login alone will trigger the above check for a corresponding CiviCRM contact. Instead, this check is made whenever a logged in Joomla user engages in a transaction with the CiviCRM system, such as editing a CiviCRM **Profile** form, making a **Contribution** or registering a **Membership**. You can, however, replace the Joomla registration form with a form that using a CiviCRM profile that has registration enabled.

!!! tip

    Thus, for example, if a contact has been entered in the CiviCRM database manually by an administrator, or as a result of a transaction as the anonymous Joomla user (eg in a contribution or membership transaction, or a "quick registration"), then the user needs to do more than merely create a Joomla account with matching criteria (eg email) to get linked to their CiviCRM record. They need also to engage in a CiviCRM transaction while they are logged in. Thus a process might look like:

    1. User makes a Contribution as the anonymous Joomla user i.e. no login required. Their email address and any custom Profile fields from the Contribution form is recorded in a CiviCRM record.
    1. User subsequently returns to site and registers as a Joomla user using the same email address as previously used.
    1. User logs in as the above Joomla user and is now presented with a menu item (visible to registered users only) to eg "Edit my details" which links to a CiviCRM Profile.
    1. Clicking on this menu link performs the match between the Joomla user and CiviCRM contact record, and the user is taken to their Profile edit page. The Joomla user account and CiviCRM record are now linked.

However, you can create a user plugin that responds to one or more of the user events. In Joomla 1.5 those are:

* onBeforeStoreUser
* onAfterStoreUser
* onBeforeDeleteUser
* onAfterDeleteUse
* onLoginUser
* onLogouUser

In 1.6 those are

* onUserAfterDelete
* onUserAfterSave
* onUserBeforeDelete
* onUserBeforeSave
* onUserLogin
* onUserLogout

## WordPress Behavior

CiviCRM used the add_action function to listen to the wordpress functions: 'user_register' and 'profile_update'. In both cases CiviCRM synchronizes the WP user account with the CiviCRM contact. Currently CiviCRM only sync the WP email field with the CiviCRM contact.


## Synchronize Users-to-Contacts

### Synchronize Users-to-Contacts Overview

The Synchronize Users-to-Contacts feature is most often used when an organization has a pre-existing Drupal or Joomla site and is adding CiviCRM for the first time. This allows all users of the existing Drupal or Joomla site to have CiviCRM contact records automatically generated.

In Drupal and Joomla, when someone registers with a site (or an administrator adds them), a user record is created. A user is the person who is logging into the Drupal or Joomla CMS (Content Management System). This is different from CiviCRM contact records, which usually include a much broader range of information about individuals, organizations and households.

When CiviCRM is "turned on" in Drupal or Joomla, a contact record is **automatically** created every time a user record is created. CiviCRM often has many additional contact records that are not user records (**[read more...](https://wiki.civicrm.org/confluence/pages/viewpage.action?pageId=47711133)**).

### Synchronize Users-to-Contacts

Go to **Administer CiviCRM**. In the **Users and Permissions** section, choose **Synchronize Users to Contacts**.

* User records are records generated by Drupal when someone creates a login and password for themselves to use on your Drupal Website.
* Contact records are records created in CiviCRM either through an import, data entry or the synchronize users-to-contacts function.

Synchronize Users-to-Contacts checks each user record for a contact record. If there is no corresponding contact record for a user, a new one will be generated.

Click on Synchronize Users-to-Contacts and you will see the message:
 ![](https://wiki.civicrm.org/confluence/download/attachments/47710580/SynchroMsg.jpg?version=1&modificationDate=1170939185000&api=v2)

 Click OK to proceed.

Once complete, you will see a message like this:

> Synchronize Users to Contacts completed. Checked 5 user records. Found 3 matching contact records. Created 2 new contact records.

You can then search your contact records to view or edit the new contact records. Go to **Advanced Search** , **>>Change Log** section and enter dates that include the date when the synchronization was performed.
