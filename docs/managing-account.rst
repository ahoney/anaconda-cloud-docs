=====================
Managing Your Account
=====================

Personal accounts
=================


Overview
~~~~~~~~

This section explains how to create a free or personal account, log in
and out, and access the settings and features of different types of
accounts.

Create free account
~~~~~~~~~~~~~~~~~~~

**Free account features**

All Anaconda Cloud users can find, download and use packages without
creating a subscriber account. Subscribers can upload packages,
notebooks and environments, and they get a 4-node cluster license free
of charge. They can also create organizations.

Free Anaconda Cloud accounts and organizations have the following
limitations:

-  There is only one build queue available to free users, and it builds
   packages only for Linux-64 machines, not OS X or Windows.
-  Builds run as capacity is available in this shared public queue.

You'll need to create an Anaconda Cloud account to:

-  author packages
-  access shared private packages

To sign up for a free account:

-  In a browser, go to `Anaconda Cloud <http://anaconda.org>`__.
-  Make sure the Sign Up tab is active. NOTE: There's also a Sign In tab
   for existing users. |Anaconda Cloud home page|
-  Select a username.
-  Enter your email address. NOTE: Users who register with an .edu email
   are granted a few additional features.
-  Create a password. NOTE: The password must be at least 7 characters
   long.
-  Enter the password again to confirm it.
-  Read and accept the Terms and Conditions.
-  Click the Sign up button. The system creates your free account, logs
   you in, and displays your personal Dashboard.

TIP: Anaconda Cloud displays your profile photo if the email address you
used to register on Anaconda Cloud is associated with a Gravatar
account. Go to `gravatar.com <http://gravatar.com>`__ to associate your
email address or to change your Gravatar profile photo.

While you're logged in, at the top right of each page in Anaconda Cloud,
the user toolbar displays. TODO - LINK IN IMAGE managing-toolbar-menu.png 

The drop-down menu contains the following options:

#. Landscape - Your home page.
#. View All - All packages, notebooks and environments you have created.
#. Packages - Only packages you have created.
#. Notebooks - Only notebooks you have created.
#. Environments - Only environments you have created.
#. Groups - If you are part of an organization, the groups you can access.
#. Labels - Labels you have created, for example test or development. See 
documentation for additional information.
#. Build Queues - If you are part of an organization and build packages, 
this is a list of queues you may access.

Packages, notebooks and environments that you have created with this account 
appear on your Dashboard. 

See Also: :ref:`Working with Packages <using-packages>`


Reset password
~~~~~~~~~~~~~~

The Sign In screen offers two links to help regain access to your
account:

-  **I forgot my username.** Click this link to have the username
   emailed to the email address of record.
-  **I forgot my password.** Click this link to have a reset password
   link sent to the email address of record. NOTE: The reset password
   link expires within 24 hours. If you no longer have access to the
   email account, you can create a new account or email
   `support@continuum.io <mailto:support@continuum.io>`__ for
   assistance.


Upgrade or downgrade plan
~~~~~~~~~~~~~~~~~~~~~~~~~

-  Log in to your Anaconda Cloud account.
-  Select the gear icon in the toolbar to access User Settings.
-  Select Billing.
-  Click the Change Plan button. The system displays detailed
   information about your plan.

NOTE: If you need more private packages or storage space than is
included in the Personal plan, `contact Continuum
Analytics <https://www.continuum.io/contact-us>`__ so we can customize a
plan for you.

NOTE: If you need assistance with billing questions, please `contact
Continuum Analytics <https://www.continuum.io/contact-us>`__.


Create organization
~~~~~~~~~~~~~~~~~~~

To create an organization:

-  Log in to `Anaconda Cloud <http://anaconda.org>`__.
-  Click the User Settings (gear) icon in the toolbar.
-  Select the Organizations option. The system displays Organizations
   settings.
-  Click the Create a new organization button. The system displays the
   Create a New Organization screen.
-  Supply an organization name. NOTE: Organization names cannot include
   spaces or special characters.
-  Supply an email address, then click the Create Organization button.
   The system displays the dashboard for the new organization.

As the creator and owner of an organization, you have automatic
administrative access to this organization and any packages associated
with the organization.

The Organization Settings screen shows a list of all organizations to
which you belong.

NOTE: The Organization Settings screen only lists organizations for
which you are an administrator, and will not display organizations for
which you are a user but not an administrator.


Delete an organization
~~~~~~~~~~~~~~~~~~~~~~

To delete an organization you administer and erase all data associated
with it:

-  Select User Settings in the toolbar.
-  Click the Account option. The system displays the Account Settings
   screen.
-  Select the appropriate organization from the dropdown menu on the
   right.
-  Under the Delete Account? section, click the Delete button. The
   system displays a confirmation screen.


Customize users and groups
~~~~~~~~~~~~~~~~~~~~~~~~~~

Administrators may add, remove or edit group and user access. To access
these features, choose User Settings from the toolbar, then click the
Groups option. The system displays the Groups Settings:

You can also navigate directly to the settings for an organization you
manage from the drop-down menu on the right.

After switching from your user view to an organization view, you can
review and edit the current group and user access for an organization,
as well as add new groups and users::

        https://anaconda.org/organization/<OrgName>/settings/groups/

Users will receive a dashboard notification when you add them to an
organization.


Customizable groups for differing access levels
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Within an organization, you can create a group to customize access for a
group of users:

-  From your dashboard, choose the User Settings (gear icon) from the
   toolbar.
-  Select the Organizations option.
-  Select the Settings link next to the organization's name.
-  Select the Groups option.
-  Click the +New Group button. Give the group a name, and assign the
   desired permissions (Read-Only, Read-Write, or Administration).
-  Click the Save Group button.

Customize per-package access by group
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Organization administrators can give groups access to a package.

-  From your dashboard, choose the User Settings (gear icon) from the
   toolbar.
-  Select the Organizations option. NOTE: The Groups function is only
   available under an Organization profile settings, and is not
   available under an individual's profile settings.
-  Select an organization you administer by clicking on the organization
   name. The system shows packages associated with that organization.
-  Select the package you want to share with the group by clicking on
   the package name. The system shows options for managing that package.
-  Click Settings to access Package Settings.
-  Click the Collaborators option. The system displays any groups that
   have access to the package.
-  Click Add Group to create a new group, or enter the existing Group's
   name and click the Add button.


Add a collaborator to a package
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You can add other users to collaborate on your packages. You'll need to
know the username of the other user(s).

-  From your dashboard (or the dashboard of an organization you
   administer), select the package for which you want to add a
   collaborator by clicking on its name.
-  Click the Settings option. The system displays package settings.
-  Click the Collaborators option.
-  Enter the username of the person you want to add as a collaborator
   and Click the Add button.


Remove a collaborator from a package
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To revoke package access previously granted to a collaborator:

-  From your dashboard (or the dashboard of an organization you
   administer), select the package for which you want to add a
   collaborator by clicking on its name.
-  Click the Settings option. The system displays package settings.
-  Click the Collaborators option. The system shows current
   collaborators.
-  Click the red X button next to a collaborator to revoke their access.


Transfer a package to a new owner
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

By default, when you create or add packages, they are attached to your
individual profile. You can transfer ownership to another owner account
you control; for example, to an Organization profile you manage. To
transfer a package to a new owner:

-  From your dashboard (or the dashboard of an organization you
   administer), select the package for which you want to transfer
   ownership. The system displays options for that package.
-  Click the Settings option. The system displays package settings.
-  Click the Admin option.
-  Under Transfer this package to a new owner, click the Transfer
   button.
-  Select the organization name for the new owner and click the Transfer
   Ownership button.


Academic Accounts
=================

Overview
~~~~~~~~

Anaconda Cloud is free for academic users. Users who subscribe to
Anaconda Cloud with an email address from an .edu domain are
automatically granted access to add-ons, including IOPro, MKL and
Anaconda Accelerate.

If you need assistance with an academic account, email us at
`support@continuum.io <mailto:support@continuum.io>`__.


Organization Accounts
=====================

Subscribers - in both free and paid accounts - can create Anaconda Cloud
organizations. Create an organization to:

-  Share packages, environments or notebooks under an organization's
   account rather than your personal account
-  Assign multiple account administrators
-  Assign different access permissions to groups of users and customize
   per-package access by group
-  Host more, larger packages. See `our
   pricing <https://anaconda.org/about/pricing>`__ for details.


Free vs. paid Organization Features
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In a free plan, organizations have the following limitations:

-  No private packages allowed
-  Build packages for Linux-64 with the public queue on Anaconda Cloud

In a paid plan, organizations can:

-  Host up to 100 private packages
-  Use up to 100 GB of Storage
-  Configure build workers and attach them to private build queue(s) -
   build your own cross-platform packages

See `our pricing <https://anaconda.org/about/pricing>`__ for details.

.. |Anaconda Cloud home page| image:: /img/cloud-home.jpg
.. |Anaconda Cloud user toolbar| image:: /img/cloud-user-toolbar.jpg
