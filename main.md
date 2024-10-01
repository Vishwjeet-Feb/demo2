<img src="./media/f206b6dee2c05a2ab4b21406bb71a625d19df3c4.png"
style="width:6.1875in;height:2.39583in" />

# Level-up CSP Technical Training – Power Platform Facilitator Guide

## Build a copilot for your customer’s webpage

## Lab Guide for Retail Scenario

| Description | Develop a Virtual Assistant copilot for Contoso Electronics' website to enhance customer support by simplifying the laptop discovery process, providing tailored recommendations, and offering side-by-side device comparisons. The copilot will also inform customers about current deals, accessories, and protection plans. Additionally, it will assist with appointment scheduling for further consultation with sales associates. To streamline the post-purchase process, the copilot will provide information on Contoso’s return policies, check return eligibility, and enable customers to submit refund requests directly within the chat interface for a seamless user experience. |
|:---|----|
| Prerequisites | To get the most out of this lab guide we recommend you have Work, School or Admin Tenant ID and Password. Trial access with Power Apps, Power Automate Flow, Copilot Studio, Dynamic 365 Customer Service and Return policy lab file. |
| Duration | 2 hours |
| Version | 1.0 |
| Publication date  | September 2024 |

This document is provided “as-is”. Information and views expressed in
this document, including URL and other Internet Web site references, may
change without notice. You bear the risk of using it. 

This document does not provide you with any legal rights to any
intellectual property in any Microsoft product. You may copy and use
this document for your internal reference purposes. 

 

© 2024 Microsoft. All rights reserved.  



# **Objective & Scenario**

## Objective

Develop a standalone Virtual Assistant copilot for Contoso Electronics'
webpage to assist customers in discovering the best products based on
their specific needs and preferences, as well as handling post-purchase
activities like verifying return eligibility and submitting refund
requests seamlessly.

## Solution Focus Area

Contoso Electronics, a leader in consumer electronics, offers a wide
variety of devices and accessories, making it challenging for customers
to find the right product that meets their unique requirements and book
appointment for sales assistance. In addition, customers may need
assistance with returns and refunds for products that do not meet their
expectations.

Currently, customers face two main challenges:

1.  **Product Discovery:** Customers struggle with exploring the vast
    array of options, comparing specifications, and understanding
    promotions and deals, which delays purchasing decisions and book
    appointment for further sales assistance.

2.  **Return Process:** Customers experience difficulties in navigating
    Contoso’s return policies and efficiently submitting refund
    requests.

To enhance customer satisfaction and streamline both the discovery and
post-purchase processes, Contoso Electronics will deploy a Virtual
Assistant copilot on its website. This AI-powered assistant, enhanced
with knowledge sources, will assist customers from the initial product
discovery phase through to post-purchase services like returns and
refunds.

## Persona and Scenario

- **Remy Morris** - Digital Solutions Architect 

<!-- -->

- **Mark Brown** – Project lead 

<!-- -->

- **David Flores** – App developer 

<!-- -->

- **Jane Miller** – App tester 

- **Grady Archie –** Customer (Product Discovery)

- **Miriam Graham –** Customer (Refund Request)

These personas will participate in the following sequential scenarios: 

- Remy Morris, Digital Solutions Architect at Contoso Electronics,
  creates and plans digital architecture that aligns with the business
  need and articulates this framework to Mark Brown, the Project Lead at
  Contoso Electronics, and assists him in selecting the most suitable
  Power Platform tools for the implementation of the digital solutions. 

<!-- -->

- Mark Brown provides David Flores with an overview of the tools and
  processes involved in developing a virtual agent with copilot studio
  and power apps and creating a booking appointment and refund request
  flow using Power Automate. 

<!-- -->

- David successfully creates a virtual assistant, fulfilling all the
  requirements of Contoso electronics to provide virtual assistance for
  product information, booking assistance appointment and submit refund
  requests, which he then submits to Jane Miller for testing. 

<!-- -->

- After thorough testing and validation, Mark Brown officially deployed
  a virtual agent on Contoso electronics website for virtual assistance
  to the customer and streamline the refund or return process.

- Grady Archie, a returning student, visits the Contoso Electronics
  website to find a laptop for his studies, gaming, and video editing.
  He engages with the Virtual Assistant copilot and outlines his
  specific needs, including battery life, durability, and performance.
  The copilot provides him with recommendations, compares specs,
  highlights current deals on Microsoft Surface laptops, and suggests
  compatible accessories. Grady decides to purchase the Surface Laptop
  Studio 2 but opts to schedule an appointment with a sales associate
  through the copilot to finalize his decision.

- Miriam Graham, a frequent shopper, wants to return a laptop due to
  unsatisfactory battery life. She interacts with the Virtual Assistant
  copilot to check if she is eligible for a return. The copilot quickly
  accesses Contoso’s return policies and confirms her eligibility.
  Miriam then asks the copilot to assist with submitting a refund
  request. The copilot guides her through the form submission process,
  enabling her to complete the refund request within the chat window.

## Pre-requisites 

For this use case, all participants will need the following: 

- Work, School or Admin Tenant Email Id and Password.

- Microsoft Power Apps Free Trial License

- Microsoft Power Automate Free Trial License

- Microsoft Copilot Studio Free Trial License

- Microsoft Dynamic 365 Customer Service Free Trial License

- Contoso Refund Policy File.

**Note:** Please be aware that the user interface (UI) of Power Apps,
Copilot, Microsoft 365, Power Automate, and other related tools may
change over time as Microsoft continues to update its products. However,
the core concepts and logic behind their functionality will remain
consistent. The principles you learn in this lab can still be applied,
even if the UI looks different in the future.



# **Lab Instructions**

# Exercise 1: Setting Up and Configuring Dynamic 365 Customer Service

In this exercise, you'll set up and configure Dynamics 365 Customer
Service by signing up for a trial, managing users, and configuring
essential settings. Follow these steps to get hands-on with the
platform's core features and start optimizing your customer service
operations.

## Task 1: Sign Up for Dynamics 365 Customer Service Trial

1.  Begin by opening your preferred web browser and navigating to the
    <https://www.microsoft.com/en-us/dynamics-365/products/customer-service>
    page.

2.  On the homepage, locate and click on the **Try for free** button.
    This will initiate the process to sign up for a free trial of
    Dynamics 365 Customer Service, allowing you to explore its features
    and capabilities.

<img src="./media/585ca016cd1e040c27372302b76435c84c136b03.png"
style="width:6.26806in;height:3.32708in" />

3.  After clicking the button, you will be redirected to a page where
    you need to enter your Work, School or Admin Tenant Email ID. For
    this lab, we use an admin tenant ID, but participants can use any of
    these options.

**Note:** If your work, school, or admin tenant email ID works fine, you
can use it to sign in without any issues. However, if you're
experiencing problems with your current ID or if you don't have a work,
school, or admin tenant ID, you will need to create one. To do so, use
the following link to set up a new ID: [Create New
ID](https://go.microsoft.com/fwlink/?LinkId=2139833&ru=https%3A%2F%2Fwww.microsoft.com%2Fen-us%2Fdynamics-365%2Fproducts%2Fcustomer-service%3Ftsapp%3Dcustomerservice%26trialflow%3Dadmin&email=bumblebee.code%40outlook.com).
This will allow you to complete the registration and resolve any sign-in
issues.

4.  Once you have entered the ID**,** Select the checkbox and click on
    **Start your free trial** to proceed.

<img src="./media/3ccdfd3011924d9b9f9f41b272436cbdc9a47e96.png"
style="width:6.26806in;height:4.95833in" />

5.  Then Enter the **password** required for the login and then click on
    **Sign in.**

6.  On the next screen, you will be asked to provide additional details
    to complete the setup. Select **Country (We choose United States)**
    as **region**.

7.  Enter your **Phone Number** in the provided field for verification
    purposes. This helps Microsoft ensure that the trial is being
    accessed by genuine users.

8.  Once all information is entered, Select the cleck box and click on
    **Submit** to finalize the setup.

<img src="./media/e71cc0dcf52443db80249f7e1e817a530d637af2.png"
style="width:6.26806in;height:4.19167in" />

9.  After successfully submitting your information, the system will
    automatically redirect you to the **Dynamics 365 Customer Service**
    workspace.

10. This workspace serves as the central hub where you can access
    various customer service tools and functionalities within Dynamics
    365.

11. Within the workspace, you'll find several applications that are
    crucial for managing customer service operations. Turn of the new
    look and click on **Customer Service workspace** to open and explore
    these apps.

<img src="./media/d900e949af91d1d25df1ef1ad06b6209ea3c67b4.png"
style="width:6.13715in;height:2.9375in" />

12. Next, locate and click on the **Customer Service admin Center**
    within the workspace. The admin centre is where you can configure
    settings, manage users, and customize various aspects of your
    customer service setup.

<img src="./media/e63de255877073609436a9e48fa9564f41deb93b.png"
style="width:6.26806in;height:2.94931in" />

13. In the admin Center, go to the **Customer Support** group and select
    **Routing**. This section allows you to manage how customer service
    requests are routed to the appropriate channels or agents within
    your organization.

Note: If participants are using school or work email ID, no need to
perform this step.

**Screenshot: Admin Tenant ID**

<img src="./media/f1049dd14d7a6af78f7192f581a7353752351673.png"
style="width:6.26806in;height:2.94931in" />

14. On the Routing page, scroll down to locate the Record Routing
    section. Here, you will find an option labelled **Turn on Unified
    Routing for Records**. Click **Manage** next to this option to open
    the settings.

Note: If participants are using school or work email ID, no need to
perform this step.  
  
**Sceenshort: Admin Tenant ID**

<img src="./media/7a254d836e327352c3636d876c5b02f0058ed523.png"
style="width:6.26806in;height:2.42292in"
alt="A screenshot of a computer Description automatically generated" />

15. You will be taken to the Service Configuration Settings page. Under
    the Unified Routing section, ensure that the Turn on Unified Routing
    toggle is switched to Yes. If it is not set to Yes, please turn it
    on.

Note: If participants are using a school or work email ID, this step are
not necessary.

> **Sceenshort: Admin Tenant ID**
>
> <img src="./media/844cf47c6ccb49090aaeba4278ddb08ad7f6381e.png"
> style="width:6.26806in;height:2.76181in" />

16. Finally, click **Save** to apply the configuration changes. If
    participants are using a school or work email ID, these steps are
    not necessary.

<img src="./media/4612686dc415fe0c259f5bbb408604f41e99c998.png"
style="width:6.26806in;height:2.9625in" />

## Task 2: Manage a User in Omnichannel for Customer Service

1.  Start by accessing the **Dynamics 365 Customer Service admin
    center**.

2.  In the site map on the left, locate and select **User management**
    under the **Customer support group**.

3.  On the **User management** page, find the **Users** section.

4.  Click on the **Manage** button next to **Users** to open the list of
    users within your organization.

<img src="./media/cf32021210c4e34515a38e8d0f8c4b24f9ca646c.png"
style="width:6.26806in;height:2.37847in"
alt="A screenshot of a computer Description automatically generated" />

5.  To focus on users who are part of the Omnichannel for Customer
    Service, click the dropdown next to **Enabled Users**.

6.  From the dropdown menu, select **Omnichannel Users**. This filters
    the list to show only those users who are active in the Omnichannel
    environment.

<img src="./media/4ee8f78469727b6ea18bcdd9326913c80202723d.png"
style="width:6.26806in;height:2.97361in" />

7.  Click on the Omnichannel username to open the specific settings and
    configurations for that user. In our admin tenant, the **username**
    is displayed as **MOD Administrator**. If participants are using
    their work, School or Tenant ID, their username may be change and
    shows **like “John”, "Admin" etc.**  
      
    <img src="./media/43ba9bbb51e092bd0bb1f1060935b436c09943db.png"
    style="width:6.26806in;height:2.91042in"
    alt="A screenshot of a computer Description automatically generated" />

8.  Once you are on the user page, locate and select the **Omnichannel**
    tab. This tab contains settings specific to Omnichannel
    functionality, allowing you to manage how the user interacts within
    the Omnichannel environment.

<img src="./media/cda841681665a38fac65c8bf914a0e66871ba349.png"
style="width:6.26806in;height:3.43819in"
alt="A screenshot of a computer Description automatically generated" />

9.  On the Omnichannel tab, you will confirm the following settings. If
    the current setting differs, please adjust the value as indicated
    below:

    1.  Capacity: Set the value to 100. This defines the user's workload
        capacity within the Omnichannel environment.

    2.  Default Presence: Set this to Available. This specifies the
        user's default status when logged into the Omnichannel system.

> <img src="./media/e904756745502529e65b1f18ab51935f00b593e2.png"
> style="width:6.26806in;height:2.57014in"
> alt="A screenshot of a computer Description automatically generated" />

10. Click on **Save and close** to finalize the user settings and exit
    the configuration page.

> <img src="./media/f0d83fded604ab405f4970cedf48b8dce4f9f9ea.png"
> style="width:6.26806in;height:2.55417in"
> alt="A screenshot of a computer Description automatically generated" />

## Task 3: Configure Omnichannel Power Virtual Agent Extension

1.  Start by navigating to the
    <https://appsource.microsoft.com/en-cy/product/dynamics-365/mscrm.omnichannelpvaextension?tab=Overview&ref=dynamicsforcrm.com>
    page. If required, sign in with **same ID and password** which used
    in Dynamic 365 Customer Service.

2.  On this page, click the **Get it now** button. This initiates the
    installation of the extension, which is essential for integrating
    Power Virtual Agents into your Omnichannel setup.

3.  After clicking **"Get it now,"** you'll be prompted to select an
    environment where the extension will be installed.

<img src="./media/c9e9bafc83006cfec41b5fcd08ea91b02cff954f.png"
style="width:6.26806in;height:2.99306in"
alt="A screenshot of a computer Description automatically generated" />

4.  Choose Environment **CustomerService Trial** from the dropdown menu,
    select both checkboxes then click **Install.**
    <img src="./media/40302f1d6d36fab271d6d64bf8ec66f40dc2dd2c.png"
    style="width:6.26806in;height:2.97708in" />

5.  Once the extension is installed, Dynamic 365 apps page will open,
    you’ll need to update all Dynamics 365 apps to ensure they are
    compatible with the new extension. Look for any app that have an
    **Update available** status and click on the **update available.**

<img src="./media/f6435f4b9c0f86a96ce196207b34bd852b7095d7.png"
style="width:6.26806in;height:3.57917in"
alt="A screenshot of a computer Description automatically generated" />

6.  For each app with an update available, select the checkbox to agree
    to the terms, then click **Update**. This step is crucial to ensure
    all components work together seamlessly.

> <img src="./media/eeb6e2fc8643ca303175ee3260b99c3326f96e59.png"
> style="width:4.81667in;height:5.03333in"
> alt="A screenshot of a computer Description automatically generated" />

## Task 4: Configure Search Settings in the Power Platform Admin Center

1.  First, log in to the <https://admin.powerplatform.microsoft.com/>
    using same credentials.

2.  After logging in, navigate to **Environments** on the left-hand side
    and select **CustomerService Trial** environment from the list.

<img src="./media/257e934cd501eb97a94893cd3918f2af2e8a8f7d.png"
style="width:6.26806in;height:2.97222in" />

3.  In the CustomerService Trial environment, locate the top pane, click
    the dropdown next to **Resource**, and select **Dynamics 365 apps**.

<img src="./media/f56afe5bb1a471ceb208a15038094ee790a62429.png"
style="width:6.26806in;height:2.9625in" />

4.  Ensure that **Omnichannel for Customer Service** is installed. This
    confirms that the Omnichannel features are active in your
    **CustomerService Trial** environment, enabling you to configure the
    necessary settings.

<img src="./media/9bf881e44309e59d9a7f4d8e48f73dce8dabcde8.png"
style="width:6.26806in;height:3.85208in"
alt="A screenshot of a computer Description automatically generated" />

5.  Go back to the **Environments -\> CustomerService Trial** page in
    the admin center.

<img src="./media/257e934cd501eb97a94893cd3918f2af2e8a8f7d.png"
style="width:6.26806in;height:2.97222in" />

6.  Click on **Settings** in the top pane, which will bring up various
    configuration options.

<img src="./media/d2290adffebe8bf490e6b2d3bf4058bfc954c535.png"
style="width:6.26806in;height:2.95139in" />

7.  Under **Product**, select **Features**. This section allows you to
    enable or disable specific features related to search functionality.

<img src="./media/9c15d9a10c5e22e2ac69a34fb99d58e624419423.png"
style="width:6.26806in;height:4.12778in"
alt="A screenshot of a computer Description automatically generated" />

8.  In the **Features** section, you’ll find several options related to
    search. You’ll need to toggle the following settings to **ON**:

    1.  **Dataverse Search**: This feature enhances the overall search
        capability, making it easier to find records across the
        Dataverse.

    2.  **Single Table Search**: This allows you to perform searches
        within a specific table, which can improve the accuracy of
        search results.

<img src="./media/a1c4898dde3c0cd70a12e7d39abc1452e267e6bc.png"
style="width:6.26806in;height:3.67986in"
alt="A screenshot of a computer Description automatically generated" />

9.  After toggling the search settings to **ON**, scroll down to the
    bottom of the page.

10. Click the **Save** button located at the bottom right to apply the
    changes. This step ensures that your configurations are active and
    ready for use in your environment.

<img src="./media/40dab952077e6342d18708f9dd51a9bf4593b653.png"
style="width:6.26806in;height:4.30208in"
alt="A screenshot of a computer Description automatically generated" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Set up and configured **Dynamics 365 Customer Service** with Unified
    Routing.

2.  Managed users in **Omnichannel**, optimizing their capacity and
    availability.

3.  Installed and configured the **Power Virtual Agent Extension** for
    enhanced customer interactions.

4.  Enabled advanced **search features** in the Power Platform,
    improving data accessibility and search accuracy.

This ensures a fully functional customer service environment with
streamlined operations.

# Exercise 2: Signup for Power Apps and Copilot Studio

In this exercise, we will focus on signing up for Microsoft Power Apps
and Copilot Studio. This process will enable you to access and leverage
these platforms for developing and integrating automated solutions. You
will begin by creating your accounts and setting up the necessary
environments to start building and configuring your applications and
Copilot functionalities.

## Task 1: Sign Up for Microsoft Power Apps

1.  Open your web browser and go to the
    <https://powerapps.microsoft.com/free/> page.

2.  On this page, locate the **Try free** button and click on it to
    begin the sign-up process.

<img src="./media/493ac0c16dd229deba1203a964f9faae8b2df3b9.png"
style="width:6.26806in;height:2.96875in" />

3.  Under the "Let's get started" section, you'll see a text box
    labelled **Enter your work or school email to get started**. Type in
    your same ID here which we use in **Dynamic 365 Customer Service.**

4.  After entering your **ID**, check the agreement box to agree to the
    terms and conditions.

5.  Click on **Start free** to proceed.

<img src="./media/263b16309cc74cba9936499671fc540ed2891ea8.png"
style="width:6.26806in;height:2.93472in" />

6.  If you receive a prompt stating that you already have a Microsoft
    account associated with the entered email address, select **Sign
    in**. Enter your same **ID and Password** when prompted.

7.  After signing in, you may be prompted with an option to stay signed
    in. Select **Yes** to stay signed in for quicker access in the
    future.

8.  Once you're signed in, look at the top-right corner of the screen.
    Choose the environment **CustomerService Tria**l. This is important
    for the next steps, as you’ll need to select this environment when
    working in Power Apps.

## Task 2: Sign up for Copilot Studio

1.  Navigate
    to [https://copilotstudio.microsoft.com](https://copilotstudio.microsoft.com/) and
    click on **sign in.**

2.  Pick an account window will pop up, select your same account. If
    prompted to sign in, enter your same ID and Password which we use in
    power apps, then select Sign in.

> <img src="./media/a5260519474b2de87f279a5459b8d9bacd5f008e.png"
> style="width:6.26806in;height:2.83958in" />

3.  In the **Welcome to Copilot Studio** popup, leave the country/region
    as the default value and select get started.

> <img src="./media/47312e73fc0b62660f62e5792595a278fa4bcab9.png"
> style="width:6.26806in;height:2.96389in" />

4.  At the Welcome to Copilot Studio! popup, select Skip.

5.  At the top right of the screen, select **CustomerService Trial**
    environment from the previous step.

## 

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Signed up for **Microsoft Power Apps** and selected the **Customer
    Service environment**.

2.  Registered for **Copilot Studio**, linking it to your environment
    for building AI-driven solutions.

This prepares you for creating and managing apps with enhanced customer
service features.

# Exercise 3: Create Custom Tables

In this exercise, you'll create custom tables in Power Apps to manage
data efficiently. You'll start by setting up a solution and assigning it
as your preferred solution. Then, you'll create and configure two
tables: "Book Appointments" and "Refund Requests," adding relevant
columns to capture all necessary information. Follow these steps to
build and organize your data tables effectively.

## Task 1: Create a Solution in Power Apps

1.  Navigate to the Power Apps Maker Portal at
    <https://make.powerapps.com> using your web browser.

2.  Ensure you are signed in with the same credentials and select the
    **CustomerService Trial** environment from the top-right corner.

<img src="./media/7cb7e0e94f020d0427b5b70607eab73bd8b25e2d.png"
style="width:6.26806in;height:2.97847in" />

3.  On the top right-hand side, turn **off** the **“Try the new data
    experience”.**

<img src="./media/2f0a57cc7096cd514719bce5fb75436238052f2a.png"
style="width:6.26042in;height:2.9375in" />

4.  In the left-hand navigation pane, find and select **Solutions**.

<img src="./media/8d5fa607ec9eca73dc0b8e6883790cbcc2662a99.png"
style="width:6.26806in;height:2.92778in" />

5.  Once in the Solutions section, click on **+ New solution** to create
    a new solution.

<img src="./media/ab200f2a3acf189a90dac6128075b4afbdffa335.png"
style="width:6.26806in;height:2.94097in" />

6.  In the **New solution** form, enter **Contoso Electronics** as the
    Display Name for your solution. This name identifies your solution
    within the environment.

7.  Next, you need to assign a publisher to your solution. Click on **+
    New publisher** to create a new one.

<img src="./media/0c5c23441b4fedbe76329204ec36c2cb6cd8f001.png"
style="width:6.26806in;height:2.98056in" />

8.  Fill in the following details in the publisher form:

    1.  **Display name**: Contoso

    2.  **Name**: contoso

    3.  **Prefix**: contoso

9.  After entering these details, click **Save**.

<img src="./media/6da1bf7f96e8c40469763ab17d2b617f25e01121.png"
style="width:6.26806in;height:2.975in" />

10. Once the publisher is created, select **Contoso (contoso)** from the
    Publisher dropdown.

11. Click on **Create** to finalize your new solution.

> <img src="./media/23afb883482b51cb4d3985cbecc87237554bb016.png"
> style="width:6.26806in;height:3.00972in" />

12. After creating your solution, click on **Back** in the left corner
    of the screen. This takes you back to the main Solutions page, where
    you can see your newly created solution listed.

<img src="./media/ee11530d85f91e5f4776a06378660061848a8315.png"
style="width:6.26806in;height:2.99444in" />

## Task 2: Set the Preferred Solution

1.  In the Power Apps Maker portal, navigate to the **Solutions**
    section in the left-hand menu.

2.  Locate the option **Manage** under **Current preferred solution**
    and click on it.

<img src="./media/c00e2096ad11cdf8cc1c69870e6ff94721b9865e.png"
style="width:6.26806in;height:2.96875in" />

3.  A list of available solutions will be displayed. Find and select
    **Contoso Electronic (contoso)** from the list.

4.  Once selected, click on **Apply** to set this solution as your
    preferred choice.

<img src="./media/f2ab20a6b70afbd8fd82739321f5b8b73909bc6e.png"
style="width:6.26806in;height:2.97778in" />

## Task 3: Create the "Book Appointments" Table

1.  In the Power Apps Maker portal, select **Tables** from the left-hand
    navigation pane.

<img src="./media/cb2d17bd510ac4e5e31cc9635e36afcd8b77f524.png"
style="width:6.26806in;height:2.96736in" />

2.  Click on **+ New table**, and then choose **Add columns and data**
    to start creating your new table.

<img src="./media/c78f6107391d1a56071cd01f3ed0fd3313e5f660.png"
style="width:6.26806in;height:2.96528in" />

3.  By default, the new table will be named "New Table." Click the edit
    button next to table name and rename it to **Book Appointments** and
    click on **Save** button.

<img src="./media/e7def46c10c3302c232d4f07f685b90d0319c366.png"
style="width:6.26806in;height:2.98056in" />

4.  **Appointment Type Column:**

    1.  Click on the down arrow next to the first column, and then
        select the edit column button.

> <img src="./media/fa95c1ee9be424bc8ac70795694680f752bbcfb2.png"
> style="width:5.875in;height:2.77933in" />

2.  Change the display name to **Appointment Type** and click on
    **Save**.

> <img src="./media/105aad0521fc01c7b47317b718d35622bdcc578a.png"
> style="width:5.93056in;height:2.82007in" />

5.  **Full Name Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Full Name**, and save the column.

<img src="./media/af65cd8c356f2b0d53dd7e08444f2f7cd2ebd1b1.png"
style="width:6.26806in;height:2.96736in" />

6.  **Email Address Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Email Address**, and save.

<img src="./media/25c5d0950f74ef34345920f90d4f320105f11ea0.png"
style="width:6.26806in;height:2.96875in" />

7.  **Phone Number Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Phone Number**, and save.

> <img src="./media/141dc621cda69d557638d52f7735262009896b4f.png"
> style="width:6.02778in;height:2.85027in" />

8.  **Date Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Date**, and save.

> <img src="./media/a3f425e73e010a1f3a44ceafff188186e03707b9.png"
> style="width:6.0919in;height:2.88194in" />

9.  **Time Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Time**, and save.

> <img src="./media/6c110069f26193ad1315d12180135a6f6246d0d9.png"
> style="width:6.00586in;height:2.86319in" />

10. After adding all the necessary columns, click on the **Create**
    button to finalize and create the **"Book Appointments"** table.

> <img src="./media/2342ab92f8e72ffeaa8f1d107058e5396a32d800.png"
> style="width:6.26806in;height:2.99514in" />

## Task 4: Create the "Refund Requests" Table

1.  In the Power Apps Maker portal, select **Tables** from the left-hand
    navigation pane.

> <img src="./media/cb2d17bd510ac4e5e31cc9635e36afcd8b77f524.png"
> style="width:6.26806in;height:2.96736in" />

2.  Click on **+ New table**, and then choose **Add columns and data**
    to start creating your new table.

<img src="./media/c78f6107391d1a56071cd01f3ed0fd3313e5f660.png"
style="width:6.26806in;height:2.96528in" />

3.  By default, the new table will be named **"New Table."** Click the
    edit button next to new table rename it to **Refund Requests** and
    click on **Save** button.

<img src="./media/67738e29224c074fb5999bf8b8da5499da3f97d3.png"
style="width:6.26806in;height:2.98333in" />

4.  **Full Name Column:**

    1.  Click on the down arrow next to the first column, and then
        select the edit column button.

> <img src="./media/73fddcef4715cd42cd526c0fdd904dcab0983262.png"
> style="width:6.13647in;height:2.91458in" />

2.  Change the display name to **Full Name** and click on **Save**.

> <img src="./media/26d3b68291bdc99a0733ed069d379cf3b59434a1.png"
> style="width:6.11806in;height:2.89906in" />

5.  **Date of Purchase Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Date of Purchase**, and save.

> <img src="./media/bcde171f724cd1914d174f0819af67b3cd73bf14.png"
> style="width:6.10417in;height:2.88775in" />

6.  **Description Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Description**, and save.

> <img src="./media/979e64551361f4bc152474211e7c2f796601b3e7.png"
> style="width:6.13889in;height:2.90145in" />

7.  **Email Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Email**, and save.

> <img src="./media/4651359b73bd8b34e9bf5982359414e5555a6b6c.png"
> style="width:6.17361in;height:2.92402in" />

8.  **Order Number Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Order Number**, and save.

> <img src="./media/2cfd966affdd97964bfb03e4fd87c0b714c74710.png"
> style="width:6.15972in;height:2.92222in" />

9.  **Order Type Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Order Type**, and save.

> <img src="./media/9a7fe7798f747e2dfc667d776776ee4123fd06bf.png"
> style="width:6.13889in;height:2.91369in" />

10. **Phone Number Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Phone Number**, and save.

> <img src="./media/325396517b802e7c1699f80bfc1be02fb556fc3d.png"
> style="width:6.09028in;height:2.87645in" />

11. **Preferred Contact Method Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Preferred Contact Method**, and save.

<img src="./media/6dc71dd660b90a29e47b17dec08eaa2ab40e97f8.png"
style="width:6.11806in;height:2.87398in" />

12. **Product Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Product**, and save.

> <img src="./media/82c123960355bfd667161c55613f07ed80085bb6.png"
> style="width:6.125in;height:2.88064in" />

13. **Receipt Number Column:**

    1.  Click on the **+ (add column)** button, change the display name
        to **Receipt Number**, and save.

<img src="./media/dca9bc6c4b42f00ad58558c050833f30fc371c0d.png"
style="width:6.16583in;height:2.93194in" />

14. After adding all the necessary columns, click on the **Create**
    button to finalize and create the **"Refund Requests"** table.

> <img src="./media/0a1db86d2cc1052e3d6811f3792fce06e9978f44.png"
> style="width:6.26806in;height:3.00833in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Created a **solution** called "Contoso Electronics" in Power Apps.

2.  Set it as your **preferred solution**.

3.  Built two custom tables, **Book Appointments** and **Refund
    Requests**, each with relevant columns to manage customer data
    effectively.

This setup helps organize and structure essential customer service
information in your environment.

# Exercise 4: Build a Copilot in Microsoft Copilot Studio with New AI Capabilities

In this exercise, you will create and configure a new copilot in
Microsoft Copilot Studio to assist with Contoso Electronics services.
You’ll start by setting up the copilot, including naming it and defining
its role. Next, you'll configure security settings and enable generative
AI features. You will then clean up sample and system topics, create a
knowledge base with relevant information, and finally publish your
copilot to make it operational. Follow these tasks to set up a fully
functional and intelligent copilot for your organization.

## Task 1: Create Contoso Electronics Services Copilot

1.  Navigate to Microsoft copilot studio and sign in with same id and
    password.

2.  Once logged in, make sure you are in the right environment. if not,
    please select the right environment (CustomerService Trial)

<img src="./media/4d5b2c19f22cc0d1d490da4606dd292fb2b6d310.png"
style="width:6.26806in;height:3.00278in" />

3.  On the left navigation pane, find and click on **Create**. Then,
    select the **New Copilot** tile to begin the setup process.

**Note:** The **Create a Copilot** wizard will open. This wizard guides
you through the process of setting up your copilot by allowing you to
name it, choose the language, and optionally enable generative answers
to enhance conversations.

> <img src="./media/d1548a071032a287bece8c257a5a34fde4185e19.png"
> style="width:6.26806in;height:2.99028in" />

4.  When prompted, select **Skip to configure** to proceed without
    additional configuration options at this stage.

<img src="./media/1e9e237a7b173e29e444d7ca6eafbacee2171dc9.png"
style="width:6.26806in;height:2.97639in" />

5.  In the **Name** text box, type **Contoso Electronics Services**.
    This will be the name of your new copilot.

6.  In the **Description** text box, enter **“Provide information about
    laptops, refund policy, and facilitate bookings or appointments.”**
    This description helps define the copilot’s role and functionality.

7.  In the **Instructions** text box, type “**Create a copilot for
    topics related to providing laptop information, processing refund
    requests, and booking appointments with sales executives or for
    product returns.”** This guides the copilot in handling specific
    tasks and user interactions.

8.  Choose **English** from the language options. This will set the
    primary language for interactions with the copilot.

<img src="./media/5e128c5bbbce8de85448335614c17061cd01827d.png"
style="width:6.26806in;height:2.96736in" />

9.  Click on the three dots next to the **Create** button in the
    top-right corner of the screen. Select **Edit advanced settings**
    from the dropdown menu.

<img src="./media/a5b6e876f42a9ad267476414cb639444796a288f.png"
style="width:6.26806in;height:2.95556in" />

10. In the advanced settings, find and select **Contoso Electronics**
    within the solution dropdown option. Click on **Save** to apply the
    advanced settings and proceed.

<img src="./media/b61623be1eb542b1bb6684f8c3c467c1fac5493f.png"
style="width:6.26806in;height:2.98056in" />

11. Finally, in the top-right corner of the screen, click on **Create**
    to finalize and deploy your new copilot.

<img src="./media/25bbe604b6dcfd64174f7cfb76c7284a285e3f50.png"
style="width:6.26806in;height:2.95069in" />

## Task 2: Configure Security and Generative AI

1.  In Microsoft Copilot Studio, locate and click on the **Settings**
    option in the top-right corner of the screen. This action will open
    the settings menu.

<img src="./media/404f3a549eb5010ead317c3d6f5ad6ec1d965745.png"
style="width:6.26806in;height:2.96389in" />

2.  Within the settings menu, select the **Security** tab. This tab is
    specifically for configuring security options for your copilot.

3.  In the Security settings, find and select the **Authentication**
    tile. This section allows you to determine how users will
    authenticate to interact with your copilot.

<img src="./media/b4099652b2100761fcfe5392696f2501ad54f15f.png"
style="width:6.26806in;height:2.97014in" />

4.  Choose **No authentication** from the available options. This
    setting will allow unrestricted access to your copilot without
    requiring users to log in.

5.  Click **Save** to apply the authentication settings.

<img src="./media/aa3bac07699e096e170c8135e2eed5c45a1a61b9.png"
style="width:6.26806in;height:2.93403in" />

6.  To ensure your changes have been saved, click **Save** again if
    prompted by the system.

<img src="./media/b8be2e4407b79d480bdf47665ed9bcb4ee4a4dc5.png"
style="width:6.26806in;height:2.9625in" />

7.  On the left-hand side, above the Security tab, select **Generative
    AI**.

8.  For **“How should your copilot interact with people?”**, select
    **Generative AI** to **enable** this feature.

9.  For **“How strict should the content moderation be?”**, choose
    **Medium**. This setting balances content moderation with
    flexibility.

10. Click **Save** to apply these settings.

<img src="./media/f154555102afbd10f5ca3120f4a863093722e730.png"
style="width:6.26806in;height:2.99028in" />

11. After saving your settings, click **Close** to exit the settings
    window.

<img src="./media/9034ed1a0580c43586a2ebcc207f4d81ec5602b1.png"
style="width:6.26806in;height:2.94444in" />

12. In the Copilot pane on the left-hand side of the screen, select your
    copilot to return to the **Overview** tab. This will take you back
    to the main dashboard where you can manage your copilot.

## Task 3: Delete Sample Topics

1.  In Microsoft Copilot Studio, navigate to the **Topics** tab. This
    section allows you to manage the topics associated with your
    copilot.

<img src="./media/777ee1e837dd4a240beb548f17397394a28e9724.png"
style="width:6.26806in;height:2.97708in" />

2.  Select the **Custom** tab to view the sample topics that were
    included with the new copilot.

3.  Locate the topic titled **Lesson 1**. Click on the three dots
    (ellipsis) next to this topic to reveal more options.

4.  Select **Delete** from the options.

<img src="./media/37017aa974933b438c7e6d111dc4ec73e6ea4df2.png"
style="width:6.26806in;height:2.97708in" />

5.  Confirm the deletion by clicking **Delete** again in the
    confirmation dialog.

<img src="./media/0f3fa493ab143457321e934c367562dd13cb856c.png"
style="width:6.26806in;height:2.95833in" />

6.  Follow the same steps to delete **Lesson 2** and **Lesson 3**.
    Ensure each deletion is confirmed as done in the previous step.

## Task 4: Disable System Topics

1.  In Microsoft Copilot Studio, navigate to the **Topics** tab.

2.  After removing the sample topics, select the **All** tab to view
    both custom and system topics.

3.  Find the **Sign in** topic from the list of system topics.

4.  Toggle the switch under the **Enabled** column to **Off** to disable
    this topic.

> <img src="./media/f60ba2639e793a37ceaa62cc31d1233809d43a97.png"
> style="width:6.26806in;height:2.99306in" />

## Task 5: Create Knowledge Base for Copilot

1.  Open Microsoft Copilot Studio and go to the **Overview** tab.

2.  Scroll down and **Disable** Allow the AI to use its own general
    knowledge (preview).

<img src="./media/d5effc323b348d1db4bbcb3c4193a09b7a0bafbf.png"
style="width:6.26806in;height:2.95069in" />

3.  Navigate to the **Knowledge** section next to overview option and
    click on it.

4.  Click on the **+ Add Knowledge** button to begin adding new
    knowledge sources.

<img src="./media/fa907a10e6905d3d3d4d319fec19167bf069c3ac.png"
style="width:6.26806in;height:2.95764in" />

5.  To add knowledge about products or laptops, select the **Public
    Website** option.

<img src="./media/684ed3c63a0b4890c8c8fed05750d44ec451fa90.png"
style="width:6.26806in;height:2.96389in" />

6.  Enter the URL <https://support.microsoft.com/en-us/surface> in the
    link section. This URL leads to Microsoft's support page for Surface
    products, which will serve as a knowledge source.

7.  Click **Add** next to the link to include it in the knowledge base.

<img src="./media/d7cf906fb41967bce34fb2733d62163f03b3e622.png"
style="width:6.26806in;height:2.96736in" />

8.  Then, click **Add** at the bottom of the section to finalize adding
    this knowledge source.

<img src="./media/74e686faffca2e42dc093d749a27abc039a16efd.png"
style="width:6.26806in;height:2.94792in" />

9.  Return to the **Copilot Window** **Knowledge section**, click on **+
    Add Knowledge**, and select the **File** option.

<img src="./media/6352b684b4bdc13f0979fddfe7ceebf50cbcb90d.png"
style="width:6.26806in;height:2.96389in" />

<img src="./media/abf6528e3ec9ac214bfcc642bf46e3bf85ed1346.png"
style="width:6.26806in;height:2.99722in" />

10. Click on the **Browse** button to locate and select the **Refund
    Policy** lab file.

11. Click **Add** to include this file as part of the copilot’s
    knowledge base.

<img src="./media/509df2814c240d12de274185bf8a7f9cd1ffcb2d.png"
style="width:6.26806in;height:2.96181in" />

## Task 6: Publish Your Copilot

1.  Navigate to Overview section and In Microsoft Copilot Studio, look
    for the **Publish** button on the right side of the screen.

2.  Click on the **Publish** button to start the publishing process.

<img src="./media/43b597780de8a07b572b32c9f86fda4db4f144b2.png"
style="width:6.26806in;height:2.95764in" />

3.  A confirmation dialog may appear. Select **Publish** again to
    finalize and publish your copilot.

<img src="./media/56c6e3b03e4219bf44c4d39beead2b0ecdd46080.png"
style="width:6.26806in;height:2.97292in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Created and named a **Contoso Electronics Services Copilot**.

2.  Configured **security settings** and enabled **generative AI**.

3.  Cleaned up unnecessary sample and system topics.

4.  Created a **knowledge base** by adding relevant product and refund
    policy information.

5.  Published a fully operational **copilot** to assist with customer
    inquiries and services for Contoso Electronics.

This copilot will streamline customer interactions by providing
information about laptops, refund policies, and facilitating bookings or
appointments

# Exercise 5: Create and Manage Topics

In this exercise, you will learn how to create and manage topics within
the Copilot Studio. Topics are essential for defining how your copilot
interacts with users, responding to specific triggers, and providing
relevant information. You will create various topics such as "Product
Information," "Return Policy Information," "Compare Laptop," "Book
Appointments," and "Refund Requests." Additionally, you'll configure the
Conversation Start topic and adjust settings in the Conversational
Boosting and System Fallback topics to enhance the overall functionality
of your copilot. This exercise will help you set up and fine-tune your
copilot's ability to handle diverse customer inquiries and interactions
effectively.

## Task 1: Create a Topic "Product Information"

1.  Open Copilot Studio and select the copilot you've created for this
    project.

2.  In the top bar, select **Topics** which is located next to
    **Knowledge**.

<img src="./media/192df360bdce7c43f1f08e3c99e7c9d442974ca2.png"
style="width:6.26806in;height:2.975in" />

3.  Click on **+ Add a topic** to create a new topic. Choose **From
    blank** to start with a blank template.

<img src="./media/1d1254c7b938e7dab18c203903278defd3047597.png"
style="width:6.26806in;height:2.98264in" />

4.  In the new topic canvas, at the top of the screen, enter the name of
    the topic **"Product Information"**.

<img src="./media/c10f2a7352bf3041c371e0c15400d88c8e6f28fd.png"
style="width:6.26806in;height:2.97708in" />

5.  In the canvas, you'll see a **Trigger node**. In the **Describe**
    section, enter the following phrases to trigger this topic:

**What are some deals on student laptops right now, Student laptop
deals, laptop deals, laptop information, laptop detail, laptop feature,
laptop specification**

<img src="./media/86af6321581abaaa21261bf21033ca08f836d1b7.png"
style="width:6.26806in;height:2.95764in" />

6.  Below the Trigger node, click on the **+** sign to create a new
    node. Select **Advanced options**, then choose **Generative
    Answer**. A Generative Answer node will be created.

<img src="./media/291bcd8c2619c405eec0c40ec39330877b95fcc1.png"
style="width:6.26806in;height:2.95069in" />

7.  In the Generative Answer node, click on the **Input** option
    variable window will open.

8.  In the **Select a variable** window, select **System** and scroll
    down to choose **Activity.Text**.

<img src="./media/89b01c320e8f9d8c5f7ac6b07c950695cf67c5cb.png"
style="width:6.26806in;height:2.97847in" />

9.  In the Generative Answer node, click on the **Edit** option in the
    **Data Source** section.

10. Enable the option **Search only selected sources**.

11. Choose the **Microsoft website** from the options displayed and
    scroll down.

12. In the **Content Moderation** section, select **Medium**.

13. Scroll up and click on the **(X)** to close Create generative answer
    properties window.

<img src="./media/27b60da3e8068d57170f6a32cecb2c579eb388d6.png"
style="width:6.26806in;height:2.96736in" />

14. Click on the **Save** button to save your configurations for the
    **"Product Information"** topic.

<img src="./media/837dc432de0e936ebda9eea9f2f174962fc9654e.png"
style="width:6.26806in;height:2.95069in" />

## Task 2: Create a Topic "Return Policy Information"

1.  Open Copilot Studio and select the copilot you've created for this
    project.

2.  In the top bar, select **Topics** which is located next to
    **Knowledge**.

<img src="./media/9f4ccb35a64326cc7907e82e5c458a6df441c6c7.png"
style="width:6.26806in;height:2.96389in" />

3.  Click on **+ Add a topic** to create a new topic. Choose **From
    blank** to start with a blank template.

<img src="./media/a592446710bff86f0b9351cdfc73cab94220a389.png"
style="width:6.26806in;height:2.975in" />

4.  In the new topic canvas, at the top of the screen, enter the name of
    the topic **"Return Policy Information"**.

<img src="./media/1a02547be316a96fd652fa68b416201249af2541.png"
style="width:6.26806in;height:2.95764in" />

5.  In the canvas, you'll see a **Trigger node**. In the **Describe**
    section, enter the following phrases to trigger this topic:

**return policy, can I return a product?, what is your return policy?,
how do I return an item?, returning a purchase, information about return
policy,**

<img src="./media/f73b2c7fe119fdaaaa468df530d86aca5d60a5aa.png"
style="width:6.26806in;height:2.94444in" />

6.  Below the Trigger node, click on the **+** sign to create a new
    node. Select **Advanced options**, then choose **Generative
    Answer**. A Generative Answer node will be created.

<img src="./media/d855f800073862632a150af57eba7afc6481bf89.png"
style="width:6.26806in;height:2.96389in" />

7.  In the Generative Answer node, click on the **Input** option
    variable window will open.

8.  In the variable window, select **System** and scroll down to choose
    **Activity.Text**.

<img src="./media/33336b5ae5516aa89f76b29a75f7f95db4ab3461.png"
style="width:6.26806in;height:2.93958in" />

9.  In the Generative Answer node, click on the **Edit** option in the
    **Data Source** section.

10. Enable the option **Search only selected sources**.

11. Choose the **Return Policy** Doc from the options displayed and
    scroll down.

12. In the **Content Moderation** section, select **Medium**.

13. Scroll up and click on the **(X)** to close Create generative answer
    properties window.

<img src="./media/adcbdd6e672678286962e9057f011250f57fd401.png"
style="width:6.26806in;height:2.95069in" />

14. Click on the **Save** button to save your configurations for the
    **"Refund Policy Information"** topic.

<img src="./media/9c4b06a03544d4e882b0865ce960c8a5d2b51713.png"
style="width:6.26806in;height:2.94792in" />

## Task 3: Create a Topic “Compare laptop”

1.  Open Copilot Studio and select the copilot you've created for this
    project.

2.  In the top bar, select **Topics** which is located next to
    **Knowledge**.

<img src="./media/9f4ccb35a64326cc7907e82e5c458a6df441c6c7.png"
style="width:6.26806in;height:2.96389in" />

3.  Click on **+ Add a topic** to create a new topic. Choose **From
    blank** to start with a blank template.

<img src="./media/a592446710bff86f0b9351cdfc73cab94220a389.png"
style="width:6.26806in;height:2.975in" />

4.  In the new topic canvas, at the top of the screen, enter the name of
    the topic **"Compare laptop"**.

5.  In the canvas, you'll see a **Trigger node**. In the **Describe**
    section, enter the following phrases to trigger this topic:

> **compare laptop, compare product, laptop comparison, compare between
> laptops**

<img src="./media/174209999a33e72c9963b0962f055ebaa43dec88.png"
style="width:6.26806in;height:2.9625in" />

6.  Below the Trigger node, click on the **+** sign to create a new
    node. Select **Advanced options**, then choose **Generative
    Answer**. A Generative Answer node will be created.

<img src="./media/360a0392aadb5457b8dccd1df289f24565e70ed3.png"
style="width:6.26806in;height:2.96736in" />

7.  In the Generative Answer node, click on the **Input** option
    variable window will open.

8.  In the variable window, select **System** and scroll down to choose
    **Activity.Text**.

<img src="./media/d7de11fb8481f9c58a5208ab350dceaf5e3f23b9.png"
style="width:6.26806in;height:2.92986in" />

9.  In the Generative Answer node, click on the **Edit** option in the
    **Data Source** section.

10. Enable the option **Search only selected sources**.

11. Choose the **Microsoft website** from the options displayed and
    scroll down.

12. In the **Content Moderation** section, select **Medium**.

13. Scroll up and click on the **(X)** to close Create generative answer
    properties window.

<img src="./media/6c1a57281c4e18f40258560bd4e3820a167d0603.png"
style="width:6.26806in;height:2.93264in" />

14. Click on the **Save** button to save your configurations for the
    **"Compare Laptop"** topic.

> <img src="./media/c05018485ce41046c4c8fe91650152c8421bc057.png"
> style="width:6.26806in;height:2.97708in" />

## Task 4: Create a Topic "Book Appointments"

1.  Open **Copilot Studio** and select the copilot you've created for
    this project.

2.  In the top bar, select **Topics** which is located next to
    **Knowledge**.

<img src="./media/687375e7bc1680b18e248987d8cfb928bc1eea65.png"
style="width:6.26806in;height:2.94792in" />

3.  Click on **+ Add a topic** to create a new topic. Choose **From
    blank** to start with a blank template.

<img src="./media/4772679ca4f9c6d1da265cc363c5dd3e074a33ce.png"
style="width:6.26806in;height:2.93125in" />

4.  In the new topic canvas, at the top of the screen, enter the name
    **"Book Appointments"**.

5.  In the canvas, you'll see a **Trigger node**. In the **Describe**
    section, enter the following phrases to trigger this topic:

**book an appointment, schedule a meeting, make a reservation, set up an
appointment, arrange a consultation, virtual appointment, appointment,
schedule booking.**

<img src="./media/fb424fe97ef2fbe6f7c87171f9be985ed98f9c14.png"
style="width:6.26806in;height:2.93611in" />

6.  Below the Trigger node, click on the **+** sign to create a new
    node. Select **Send a Message Node,** a **Message Node** will be
    created. In the Message node, enter the following text:

**Thank you for choosing our virtual assistant for your laptop
consultation. We are here to help you. To book a virtual appointment,
simply complete the form below.**

<img src="./media/48fc0d59bf3bee44239684086736f692d2cd03aa.png"
style="width:6.26806in;height:2.97639in" />

<img src="./media/e42b1a69e5df12e60189f8c2740129cb9929b8d7.png"
style="width:6.26806in;height:2.88542in" />

7.  Below the Message node, click on the **+** sign to create a new
    node. Select **Ask with Adaptive Card**. An Adaptive Card Node will
    be created.

<img src="./media/b023858d1513c3cce961661ae5877a8fd3b29563.png"
style="width:6.26806in;height:2.95764in" />

8.  In the Adaptive Card node, select the **three dots** (More Options)
    and then select **Properties**.

<img src="./media/ed012db218d1a75160b021e68df0e336337e7b3e.png"
style="width:6.26806in;height:2.94444in" />

9.  In the Adaptive Card properties, below the **Edit JSON**. Paste the
    provided **JSON** code to create the adaptive card.

{

"\$schema": "<http://adaptivecards.io/schemas/adaptive-card.json>",

"type": "AdaptiveCard",

"version": "1.5",

"body": \[

{

"type": "TextBlock",

"text": "Virtual Assistant Booking",

"weight": "Bolder",

"size": "Large",

"horizontalAlignment": "Center"

},

{

"type": "Input.ChoiceSet",

"choices": \[

{

"title": "Virtual Showroom",

"value": "Virtual Showroom"

},

{

"title": "Customer Service",

"value": "Customer Service"

},

{

"title": "IT Support & Repair",

"value": "IT Support & Repair"

}

\],

"placeholder": "Placeholder text",

"id": "Appointmenttype",

"label": "Appointment Type",

"style": "expanded"

},

{

"type": "Input.Text",

"id": "fullName",

"placeholder": "Enter your full name",

"label": "Full Name",

"isRequired": true,

"errorMessage": "Full Name is required."

},

{

"type": "Input.Text",

"id": "contactPhone",

"placeholder": "Enter your phone number",

"label": "Phone Number",

"isRequired": true,

"errorMessage": "Phone Number is required."

},

{

"type": "Input.Text",

"id": "contactEmail",

"placeholder": "Enter your email address",

"label": "Email Address",

"isRequired": true,

"errorMessage": "Email Address is required.",

"style": "Email"

},

{

"type": "TextBlock",

"text": "Would you like to book a virtual appointment?",

"wrap": true,

"spacing": "Medium"

},

{

"type": "Input.Text",

"id": "appointmentDate",

"label": "Date",

"isRequired": true,

"errorMessage": "Date is required.",

"placeholder": "DD-MM-YYYY"

},

{

"type": "Input.ChoiceSet",

"choices": \[

{

"title": "12:00 PM",

"value": "12:00 PM"

},

{

"title": "01:00 PM",

"value": "01:00 PM"

},

{

"title": "02:00 PM",

"value": "02:00 PM"

},

{

"title": "03:00 PM",

"value": "03:00 PM"

},

{

"title": "04:00 PM",

"value": "04:00 PM"

},

{

"title": "05:00 PM",

"value": "05:00 PM"

}

\],

"placeholder": "Placeholder text",

"id": "appointmenttime",

"label": "Time",

"style": "expanded"

}

\],

"actions": \[

{

"type": "Action.Submit",

"title": "Book Appointments",

"data": {

"action": "bookAppointment"

}

}

\]

}

<img src="./media/90b4ab1740a812211424d78df7facb9db56ed1f2.png"
style="width:6.26806in;height:2.95556in" />

10. Select **Variables** to open the Variables pane.

11. Select all the boxes on the right-hand side for the topic variables.

<img src="./media/1cb393ced714df5d48a62457c0f042fddefcabe6.png"
style="width:6.26806in;height:2.95069in" />

12. Click on **Save** to save your configuration.

<img src="./media/bf430224d1bd2857c95de51ef30f552abe4e1ff0.png"
style="width:6.26806in;height:2.98056in" />

13. Below the Message node, click on the + **sign** to create a new
    node. Select **Ask a Question**. A **Question Node** will be
    created.

<img src="./media/5fc553d57e54f3f85259a7b531c4c6894ee8c3e9.png"
style="width:6.26806in;height:2.96736in" />

14. In question node select **Enter a Message** and enter the following
    text:

> Thank you, Full Name! Your Appointment Type appointment has been
> booked for Appointment Date at Appointment Time. Thank you for using
> our service.

<img src="./media/006aec210fb2ba0a7f49e69e89759b095a8942d5.png"
style="width:6.26806in;height:2.96528in" />

15. Replace the placeholders Full Name, Appointment Type, Appointment
    Date, and Appointment Time with the appropriate variables by
    clicking on the **{X}** icon and selecting the corresponding custom
    variables.

<img src="./media/1ebc3d0c3eeb8603936e528c1ee85a98175c6580.png"
style="width:6.26806in;height:2.96042in" />

16. In the Question node, select **Multiple Choice** as the identify.

17. In the **Options for user** section, enter the following choices:

    1.  **Yes**

    2.  **No**

<img src="./media/55bf77fc7fa7d6d8abaed70011339a7f31f57086.png"
style="width:6.26806in;height:2.96389in" />

18. Below **Save the user's response** a new variable creates, click on
    the variable name variable properties window will open, where you
    can replace the variable name with **AfterAppointment**. Click the
    **(X)** to close the variable properties window.

<img src="./media/d85305f12c46c9e9ea6d76d91eedfeddd4a98f63.png"
style="width:6.26806in;height:2.95069in" />

<img src="./media/1cdf966fffb653f4ad73fed568170502154e6d14.png"
style="width:6.26806in;height:2.94444in" />

19. Under the **Yes** condition, click on the **+** sign and select
    **Topic Management**, then choose **Go to Another Topic**. A topic
    selection window will open—search for **Conversation Start** and
    select the **Conversation Start** topic.

<img src="./media/a4b04fcaa042c74b4045337f78afc1544d0e438d.png"
style="width:6.26806in;height:2.93472in" />

20. Under the **No** condition, click on the **+** sign and select
    **Send a Message**. A Message Node will be created. In the Message
    node, enter the following text:

> Thank you for using our service. Have a nice day.

<img src="./media/76bf76ffe3d451fad1c08e062c635b86a8768eec.png"
style="width:6.26806in;height:2.96736in" />

<img src="./media/caf611af4cc1e987a85640173f7dea1e0a224287.png"
style="width:6.26806in;height:2.96528in" />

21. Once all nodes are configured, click on **Save** to finalize and
    save your "**Book Appointments**" topic.

<img src="./media/256a47498cc097d5f0e620fa8caf6b6b56f5879c.png"
style="width:6.26806in;height:2.96389in" />

## Task 5: Create a Topic "Refund Requests"

1.  Open **Copilot Studio** and select the copilot you've created for
    this project.

2.  In the top bar, select **Topics** which is located next to
    **Knowledge**.

<img src="./media/adb93200c90e7aa4c01c347d84b5948342e61309.png"
style="width:6.26806in;height:2.96389in" />

3.  Click on **+ Add a topic** to create a new topic. Choose **From
    blank** to start with a blank template.

<img src="./media/7253156ac897701c44db7406e78fca4f74909157.png"
style="width:6.26806in;height:2.95208in" />

4.  In the new topic canvas, at the top of the screen, enter the name
    **"Refund Requests"**.

<img src="./media/97c726ff03795ca208efb6fa046e1f3600846c50.png"
style="width:6.26806in;height:2.95903in" />

5.  In the canvas, you'll see a **Trigger node**. In the **Describe**
    section, enter the following phrases to trigger this topic:

refund request, return request, return my product, want refund, want to
return

<img src="./media/170825ca787099a719dd0e90431c517c52efd6c6.png"
style="width:6.26806in;height:2.95764in" />

6.  Below the Trigger node, click on the **+** sign to create a new
    node. Select **Send a Message**. A **Message Node** will be created.
    In the Message node, enter the following text:

We are here to help you. To generate the refund or return request simply
complete the form below.

<img src="./media/91c56862f0ddbe1cfb840a83b1f60b404dfc23d4.png"
style="width:6.26806in;height:2.98056in" />

<img src="./media/792c6d192fa1ac5cd5e90ae70b1b56fcc9f2c1d7.png"
style="width:6.26806in;height:2.96528in" />

7.  Below the Message node, click on the **+** sign to create a new
    node. Select **Ask with Adaptive Card**. An Adaptive Card Node will
    be created.

<img src="./media/4fb0981eb3b844d3e74c94b0a7da308063fce302.png"
style="width:6.26806in;height:2.93125in" />

8.  In the Adaptive Card node, select the **three dots** (More Options)
    and then select **Properties**.

<img src="./media/5eb90ce319681b105fc238a8d25b2c1de8c25a2b.png"
style="width:6.26806in;height:2.94792in" />

9.  In the Adaptive Card properties, below the **Edit JSON** paste the
    provided JSON code to create the adaptive card.

{

"\$schema": "<http://adaptivecards.io/schemas/adaptive-card.json>",

"type": "AdaptiveCard",

"version": "1.4",

"body": \[

{

"type": "TextBlock",

"text": "Purchase Refund and Exchange Form",

"weight": "Bolder",

"size": "Large",

"horizontalAlignment": "Center"

},

{

"type": "Input.Text",

"id": "fullName",

"placeholder": "Enter your full name",

"label": "Full Name",

"isRequired": true,

"errorMessage": "Full Name is required."

},

{

"type": "Input.Text",

"id": "email",

"placeholder": "Enter your email address",

"label": "Email",

"style": "Email",

"isRequired": true,

"errorMessage": "Email is required."

},

{

"type": "Input.Text",

"id": "phoneNumber",

"placeholder": "Enter your phone number",

"label": "Phone Number",

"style": "Tel",

"isRequired": true,

"errorMessage": "Phone Number is required."

},

{

"type": "Input.Text",

"id": "product",

"placeholder": "Enter the product name or description",

"label": "Product",

"isRequired": true,

"errorMessage": "Product is required."

},

{

"type": "Input.ChoiceSet",

"id": "contactMethod",

"label": "Preferred Contact Method",

"style": "expanded",

"choices": \[

{

"title": "Phone",

"value": "Phone"

},

{

"title": "Email",

"value": "Email"

}

\],

"isRequired": true,

"errorMessage": "Preferred Contact Method is required."

},

{

"type": "Input.ChoiceSet",

"id": "orderType",

"label": "Order Type",

"style": "expanded",

"choices": \[

{

"title": "In Store",

"value": "In Store"

},

{

"title": "Online",

"value": "Online"

}

\],

"isRequired": true,

"errorMessage": "Order Type is required."

},

{

"type": "Input.Text",

"id": "receiptNumber",

"placeholder": "Enter the receipt number",

"label": "Receipt Number",

"isRequired": true,

"errorMessage": "Receipt Number is required."

},

{

"type": "Input.Text",

"id": "orderNumber",

"placeholder": "Enter the order number",

"label": "Order Number",

"isRequired": true,

"errorMessage": "Order Number is required."

},

{

"type": "Input.Text",

"placeholder": "Enter the Purchase Date",

"id": "purchaseDate",

"label": "Purchase Date",

"isRequired": true,

"errorMessage": "Purchase Date Required."

},

{

"type": "Input.Text",

"id": "description",

"placeholder": "Provide a brief description of the issue or reason for
return/exchange",

"label": "Description",

"isMultiline": true,

"isRequired": true,

"errorMessage": "Description is required."

}

\],

"actions": \[

{

"type": "Action.Submit",

"title": "Submit",

"data": {

"action": "submitRefundExchange"

}

}

\]

}

<img src="./media/a1680c51b53ba193e3888ad72b2fbe484441bf7a.png"
style="width:6.26806in;height:2.94444in" />

10. Select **Variables** to open the Variables pane.

11. Check the boxes on the right-hand side for the all-topic variables.

12. Click on **Save** to save your variable settings.

<img src="./media/3b18a772ee7996ab17210c0c8a8c03b2e607215d.png"
style="width:6.26806in;height:2.97014in" />

13. Below the adaptive card node, click on the + **sign** to create a
    new node. Select **Ask a Question, a Question Node** will be
    created.

<img src="./media/4c4569ab0e90a22e62d4846bca2c7bbf2d2fcd02.png"
style="width:6.26806in;height:2.95208in" />

14. In the Ask Question node message field, enter the message.

Thank you for using our service. You want to know more?

<img src="./media/0e865d8cc02a4b37ba55055eabfbb7c8d37b3563.png"
style="width:6.26806in;height:2.98194in" />

15. In the Question node, select **Multiple Choice** as the identify.

16. In the **Options for user** section, enter the following choices:

    1.  Shop

    2.  Deals and Promotion

    3.  IT Support and Device Repair

    4.  I’m done.

> <img src="./media/d185e5ecdab78ca737c6dab7a1a314241ab8332c.png"
> style="width:6.26806in;height:2.98194in" />

17. Below **Save the user's response** a new variable creates, click on
    the variable name variable properties window will open, where you
    can replace the variable name with **Afterrefund.**

<img src="./media/a316ea825150ab0bf8ee224d191a44fd887e1895.png"
style="width:6.26806in;height:2.96389in" />

18. Click the **(X)** to close the variable properties window.

19. Under the **Shop**, **Deals and Promotion and IT Support and Device
    Repair** condition, click on the **+** sign on each condition and
    select **Topic Management** for each, then choose **Go to Another
    Topic**. A topic selection window will open—search for
    **Conversation Start** and select the **Conversation Start** topic.

<img src="./media/c942432d01212334b03f90d0c0d61140911a79c7.png"
style="width:6.26806in;height:2.97361in" />

20. For **I’m done option,** click on the **+** sign and select **Topic
    Management** for each, then choose **Go to Another Topic** and
    select **End Conversation.**

<img src="./media/991baf14de6ee88d6d737117af009ddc661fa772.png"
style="width:6.26806in;height:2.95556in" />

21. Once all nodes are configured, click on **Save** to finalize and
    save your "Refund Requests" topic.

<img src="./media/a29a6c44bf4c24960c3fcb879a1673eeea9bb174.png"
style="width:6.26806in;height:2.94792in" />

## Task 6: Configure the Conversation Start Topic

1.  Navigate to Copilot Studio and select the Copilot you've created for
    this project.

2.  In the top navigation bar, select **Topics**, which is located next
    to **Knowledge**.

<img src="./media/d7e2f41122f9ce971a93fa8c442e28ab3b851b31.png"
style="width:6.26806in;height:2.96042in" />

3.  In the Topics section and select the **System** option to view the
    available system topics.

4.  Find and select the **Conversation Start** topic to open it.

<img src="./media/6a2ebf32d19808848227b8429df71ff71ebf8bed.png"
style="width:6.26806in;height:2.99028in" />

5.  Below the **Trigger** node, a message node is available. Replace the
    message with the given below content.

Hello! I am Contoso Virtual Agent. How May I Help You?

6.  Click the **Save** button to save your configuration.

<img src="./media/d45be8bc79d628de73e1c3a9006327c86842ca08.png"
style="width:6.26806in;height:2.96389in" />

## Task 7: Configure the Conversational Boosting Topic

1.  Navigate to Copilot Studio and select the Copilot you've created for
    this project.

2.  In the top navigation bar, click on **Topics**, which is located
    next to **Knowledge**.

<img src="./media/6a7847c627c1465bf6d37495366f0bef9ced1859.png"
style="width:6.26806in;height:2.98056in" />

3.  In the Topics section, select the **System** option to view the
    available system topics.

4.  Find and select the **Conversational Boosting** topic to open it.

<img src="./media/18a900c97cd9c8330acc088ae1f0bbea8d4480d4.png"
style="width:6.26806in;height:2.96736in" />

5.  In the **Generative Answer** node, click on Edit below the data
    source section.

6.  Toggle on the Search Only Selected Sources option.

7.  Select the **Microsoft Surface website** and the **Refund Policy**
    knowledge base as the sources for search from.

8.  Scroll down in the Generative Answer properties window.

9.  In the Content Moderation section, select the **Medium** option for
    content moderation.

10. Close the Generative Answer properties window once you're done.

11. Click on the **Save** button to save the configuration.

> <img src="./media/e8cd0c4c5456641e792a2f5e934b473da974356d.png"
> style="width:6.26806in;height:2.96528in" />

## Task 8: Use Generative Answers in the System Fallback Topic

1.  In the Copilot pane on the left-hand side of the screen, select the
    copilot you've created to return to the **Knowledge** tab.

2.  Select the Topics tab located at the top of the screen.

<img src="./media/c15e92bfabce0bf6c04cfa5aed41ad67b8a40116.png"
style="width:6.26806in;height:2.95069in" />

3.  Within the Topics tab, select the **System** option to view the
    available system topics.

4.  Find and select the **Fallback** topic to open it.

<img src="./media/6abbaeffb5615bf9c74479c46fb7d37d8c8573cf.png"
style="width:6.26806in;height:2.94792in" />

5.  In the **Fallback** topic, locate the existing message node.

6.  Click on the three dots (•••) in the top-right corner of the message
    node and select **Delete** to remove it.

<img src="./media/3568a7be46ce7b716f058438dbe40a44d28ed614.png"
style="width:6.26806in;height:2.95556in" />

7.  Below the Condition node, click on the + icon to add a new node.
    Select Advanced and then choose Generative answers from the options.

<img src="./media/a4c589b361086f07ee9223867bbf30dac2826b02.png"
style="width:6.26806in;height:2.97083in" />

8.  In the Generative answers node, for the Input field, select
    **Activity.Text** from the system variables.

<img src="./media/6b9c6804fa89812c2a58817ce2ec52974e5583a4.png"
style="width:6.26806in;height:2.96875in" />

9.  Under the **Data sources** section, click on Edit.

10. Toggle on **Search only selected sources** to ensure that the AI
    pulls information only from specific knowledge sources.

11. From the list of available sources, select the **Microsoft Surface
    website** and **Refund Policy Doc** as the knowledge source.

12. Deselect the option **Allow the AI to use its own general
    knowledge** to ensure the AI only uses the specified knowledge
    source.

13. For Content moderation, select **Medium** to manage the level of
    content filtering.

14. After completing the above steps, click **Save** to save the
    generative answers configuration for the Fallback topic.

<img src="./media/b9c8201883176397d2126f9f322f9edd942be7ac.png"
style="width:6.26806in;height:2.96736in" />

## Task 9: Publish the Copilot

1.  In the Copilot Studio, find the **Publish** button. This button is
    typically placed on the right side of the window.

2.  Click on the **Publish** button.

3.  A confirmation window may appear; click **Publish** again to
    confirm.

<img src="./media/aa96a219fa3ef2d50b663c3a3aab5bd079d1004b.png"
style="width:6.26806in;height:2.97708in" />

## Test the Copilot

1.  In the Copilot Studio, select the **Select the Three dots** located
    in the top-right corner and then select **Go to Demo Website**.

<img src="./media/c15cae8bd41de0d492a6138b86b8a42eef3de07e.png"
style="width:6.26042in;height:2.96875in" />

2.  Once the demo website launch and message appear in chat box enter
    the following trigger phrases to test the topics you created:

    1.  What are some deals on student laptops right now?

<img src="./media/457dc7bf04abe851ddca6d3c13828859708c3de2.png"
style="width:6.26806in;height:2.80208in" />

<img src="./media/af451526a0599e4552c94adaec800523098e6b8f.png"
style="width:6.26806in;height:2.96875in" />

2.  Tell me more about Surface Laptop Go 3. What are the specs & cost?

> <img src="./media/ff2da8cc5390d23dd3a13541968fd622f1ebf4bc.png"
> style="width:6.26806in;height:2.96389in" />
>
> <img src="./media/a7f6070fe603cd44f1d3b21a833e2c74aca0a4ba.png"
> style="width:6.26806in;height:2.95208in" />

3.  Compare laptop surface laptop pro 3 and surface laptop studio 2.

> <img src="./media/6bfa5731246412d23170f118e850cb3ab35b19b8.png"
> style="width:6.26806in;height:2.97917in" />
>
> <img src="./media/ee3e1faf59fb60c75a910e61977bd4acd839abaa.png"
> style="width:6.26806in;height:2.94792in" />

3.  Enter the following trigger phrases to test the topics you created:

    1.  I want to know about the Contoso refund policy.

<img src="./media/eab1032c1b79fdb4d6590fc627aad9ed6021302b.png"
style="width:6.26806in;height:2.95208in" />

<img src="./media/926b1347a5989f7d9f151365847fb4834ff4a68b.png"
style="width:6.26806in;height:2.95556in" />

2.  I buy laptop 10 days ago, is I eligible to return laptop.

<img src="./media/036f73372b5206b43805e46759039818064e7847.png"
style="width:6.26806in;height:2.93125in" />

<img src="./media/02050a644e5280279952bf0f9fa3e22d326bd08f.png"
style="width:6.26806in;height:2.96389in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  Set up and managed various topics such as "Product Information,"
    "Return Policy Information," "Compare Laptop," "Book Appointments,"
    and "Refund Requests" within Copilot Studio. Each topic is designed
    to handle specific customer inquiries using triggers and generative
    answers.

2.  Customized the initial greeting message for the copilot to greet
    users and offer assistance.

3.  Configured the Conversational Boosting topic to use selected sources
    for generating answers and set content moderation.

4.  Implemented generative answers to handle cases where the copilot
    cannot understand or respond to user queries.

These tasks collectively enhance the copilot's ability to provide
relevant and accurate information, improving the overall user
interaction experience.

# Exercise 6: Create Power Automate Flow and Integrate Actions

In this exercise, you will learn how to create and integrate Power
Automate flows with your Copilot. These flows will automate key
processes, such as booking appointments and handling refund requests.
You will configure these flows to capture and process user inputs
efficiently, and then integrate them into your Copilot to streamline
interactions. By the end of this exercise, you will have set up
automated workflows that enhance the functionality of your Copilot and
improve user experience.

## Task 1: Create Power Automate Flow to Book an Appointment

1.  In the Copilot pane on the left-hand side of the screen, click on
    your Copilot to return to the **Overview** tab.

2.  Select the **Actions** tab to start configuring actions for your
    Copilot.

<img src="./media/f4413c72d062150301aa843dcfbe79bd845c9962.png"
style="width:6.26806in;height:2.98056in" />

3.  Click on **+ Add an action**.

<img src="./media/73a4bc68e9fb2739f14f4d20cb3b5b6a0318433e.png"
style="width:6.26806in;height:2.95069in" />

4.  Scroll down and select **Create a new flow** a new Power Automate
    flow window will pop up. Check the environment from top right
    corner, if correct environment (CustomerService Trial) not selected,
    please select the correct environment.

<img src="./media/8bed6d8c4d11274241533dbe738f965d3a04fb67.png"
style="width:6.26806in;height:2.97708in" />

5.  Select **Run a flow** and rename the flow as **Book Appointments
    Flow**.

<img src="./media/c8266757bfd147cbc2c080a9549d65d5bb1f50ae.png"
style="width:6.26806in;height:2.94097in" />

6.  Select the trigger step "**Run a flow from Copilot,"** and then
    select **+ Add an input**.

<img src="./media/f43bdbd7cdf0abad7d8b1b6e12a3bee41b46d7e2.png"
style="width:6.26806in;height:2.97292in" />

7.  Select **Text** for the input type and configure the following
    inputs by repeating the process:

    1.  Enter **Type** in input field for Appointment Type

    2.  Enter **Date** in input field for Appointment Date

    3.  Enter **Email** in input field for Email Address

    4.  Enter **Name** in input field for Full Name

    5.  Enter **Phone** in input field for Phone Number

    6.  Enter **Time** in input field for Appointment Time

> <img src="./media/294334e5736354101503033d4fec6c28e3bbbe68.png"
> style="width:6.26806in;height:2.80069in" />
>
> <img src="./media/31837369d785b562f80346a50d1f91016b2341e8.png"
> style="width:6.26806in;height:2.76042in" />
>
> <img src="./media/f9bccc58ad7bd6ddcf232c1efb81f03a7b10d2da.png"
> style="width:6.26806in;height:2.96875in" />

8.  Click on the **+ icon** between the two steps in the flow and select
    **Add an action**.

<img src="./media/c8dfe6af54afe1691764ebfa53f9a4d1ff0bef9e.png"
style="width:6.26806in;height:2.94861in" />

9.  In the **Search** field, type **Dataverse** and select **See more**
    for the Dataverse connector.

<img src="./media/2a0a3c925ea92f633c5391d456ae66e564b82367.png"
style="width:6.26806in;height:2.97292in" />

10. Select **Add a new row** action.

<img src="./media/fe3fa50064d0b69c01fb0d9c142fb2dbd93c279b.png"
style="width:6.26806in;height:2.78403in" />

11. Login with the same credential for the Oauth Sign.

12. Choose **Book Appointments** for the table name.

<img src="./media/34c9080c608f3d8f63f181b1c52d3cc8be8882e8.png"
style="width:6.26806in;height:2.97292in" />

13. Select **Show all** to see all available fields.

<img src="./media/4e69c5e519dfaf13422c6f17ecb99d30da3376ae.png"
style="width:6.26806in;height:2.99792in" />

14. Use **Dynamic content** to map each input parameter to the
    corresponding field:

    1.  **Type** Dynamic Input → **Appointment Type** Parameter.

    2.  **Date** Dynamic Input → **Appointment Date** Parameter

    3.  **Email** Dynamic Input → **Email Address** Parameter

    4.  **Name** Dynamic Input → **Full Name** Parameter

    5.  **Phone** Dynamic Input → **Phone Number** Parameter

    6.  **Time** Dynamic Input → **Appointment Time** Parameter

> <img src="./media/323115f4802bd5a7cbe76ff37671953f8d0eb7cc.png"
> style="width:6.26806in;height:2.95903in" />

<img src="./media/image191.png"
style="width:6.26806in;height:2.68403in" />

15. Select **Respond to Copilot** action.

> <img src="./media/f47b5145499d3874cea7aa48cfaedd3c7c9796ac.png"
> style="width:6.26806in;height:2.9625in" />

16. Click on **Settings**.

17. Ensure that **Asynchronous Response** is set to **Off**.

<img src="./media/752f0bdf589863c85539044c2fd92a4241906c09.png"
style="width:6.26806in;height:2.95417in" />

18. Select **Save draft**.

19. Then, click on **Publish**.

> <img src="./media/691fc045987317b57fdef82ed81ce1e9acdd5ddb.png"
> style="width:6.26806in;height:2.95208in" />

20. Once the flow is published, close the Power Automate tab to return
    to Copilot Studio.

## Task 2: Create Action in Copilot for Book Appointments

1.  Go to copilot window and click on **Refresh**, (If the Copilot
    window was closed, reopen it and navigate back to the **Copilot
    Studio,** go to the **Actions** tab and click on **+ Add an
    action**.)

<img src="./media/2bd1ef07e00f9caf9698cd1d0180c52ae2dcdda0.png"
style="width:6.26806in;height:2.97639in" />

2.  In the "**Choose an action**" window, select the **Book Appointments
    Flow** you created.

<img src="./media/a21cc2dd024eed291daa78561888b8c19d451aad.png"
style="width:6.26806in;height:2.95764in" />

3.  Click on **Next**, **Next** then **Next** again, and finally
    **Finish**. The flow will now be added as an action.

<img src="./media/b30546d9ea621a4222264c0b62bff70775571f8a.png"
style="width:6.26806in;height:2.9625in" />

<img src="./media/80ad2aff66a8f757a27a3efc843804368470b582.png"
style="width:6.26806in;height:2.96806in" />

<img src="./media/e43973f45fb9bdbe33b16049666fd5b4dd17262d.png"
style="width:6.26806in;height:2.90972in" />

4.  Navigate to the **Topics** section and select the **Book
    Appointments** topic.

<img src="./media/dce7dddb625727221b78a34558127679f9bbb3e4.png"
style="width:6.26806in;height:2.91528in" />

5.  Below the Adaptive Card node, click on the **+** sign to create a
    new node.

6.  Select **Call an action**. Choose the **Book Appointments Flow**.
    This action will now be added below the Adaptive Card node.

<img src="./media/78e436022f1401977bfc22768f58f8b4270ff582.png"
style="width:6.26806in;height:2.94583in" />

7.  In the action node, you need to map each input field to the
    appropriate variable created by the Adaptive Card:

    1.  **Type** Input: Click on the input field, then select
        **Appointmenttype** from the custom variables.

    2.  **Date** Input: Click on the input field, then select
        **appointmentDate** from the custom variables.

    3.  **Email** Input: Click on the input field, then select
        **contactEmail** from the custom variables.

    4.  **Name** Input: Click on the input field, then select
        **fullName** from the custom variables.

    5.  **Phone** Input: Click on the input field, then select
        **contactPhone** from the custom variables.

    6.  **Time** Input: Click on the input field, then select
        **appointmenttime** from the custom variables.

> <img src="./media/618400bbd095eebc9b3a11e0e19370f9554c5e80.png"
> style="width:6.26806in;height:2.97292in" />

8.  After mapping all the variables, click on the **Save** button to
    save the topic configuration.

<img src="./media/53ba8f37f8b943689d18524d1e055e26b9597fcb.png"
style="width:6.26806in;height:2.95in" />

## Task 3: Create Power Automate Flow to Refund Requests Flow

1.  In the Copilot pane on the left-hand side of the screen, click on
    your Copilot to return to the **Overview** tab.

2.  Select the **Actions** tab to start configuring actions for your
    Copilot.

<img src="./media/06403961adf6a9533c536815191f6bb039266f9c.png"
style="width:6.26806in;height:2.97153in" />

3.  Click on **+ Add an action**.

<img src="./media/d9553a0f645cdd94e78aae22c1075bec21649d43.png"
style="width:6.26806in;height:2.98056in" />

4.  Scroll down and select **Create a new flow** a new Power Automate
    flow window will pop up. Check the environment from top right
    corner, if correct environment (CustomerService Trial) not selected,
    please select the correct environment.

<img src="./media/c4f71654dfd7b4eab71989b9221988107b98e5cc.png"
style="width:6.26806in;height:2.90139in" />

5.  Select **Run a flow** and rename the flow as **Refund Request
    Flow**.

<img src="./media/3bee763bb8fd333b084598435085e4feff6f12cf.png"
style="width:6.26806in;height:2.94583in" />

6.  In the trigger step "**Run a flow from Copilot,"** select **+ Add an
    input**.

<img src="./media/53da701305b380277bea6a95912f34875d61b029.png"
style="width:6.26806in;height:2.74514in" />

7.  Select **Text** for the input type and configure the following
    inputs by repeating the process:

    1.  Enter **Name** in Input for Full Name

    2.  Enter **Email** in Input for Email

    3.  Enter **Phone Number** in Input for Phone Number

    4.  Enter **Purchase Date** in Input for Date of Purchase

    5.  Enter **Description** in Input for Description

    6.  Enter **Order Number** in Input for Order Number

    7.  Enter **Order Type** in Input for Order Type

    8.  Enter **Product** in Input for Product

    9.  Enter **Receipt Number** in Input for Appointment Type

    10. Enter **Contact Method** in Input for Preferred Contact Method

> <img src="./media/112a359c5a68356162c4db6792cfcd116f31c0d8.png"
> style="width:6.26806in;height:2.73611in" />
>
> <img src="./media/03713c6f56fa9a01eee0781c673e6f3075a67fd0.png"
> style="width:6.26806in;height:2.73819in" />
>
> <img src="./media/6657d71b12c45df8b1941596988566e8ee6e35a7.png"
> style="width:6.26806in;height:2.75in" />

8.  Click on the **+ icon** between the two steps in the flow and select
    **Add an action**.

<img src="./media/3370bc31db0c8d666195da68eb0a8a6fba3b7480.png"
style="width:6.26806in;height:2.97153in" />

9.  In the **Search** field, type **Dataverse** and select **See more**
    for the Dataverse connector.

> <img src="./media/2aa8ffabc158285f49dba23822601f85b7acb87f.png"
> style="width:6.26806in;height:2.76528in" />

10. Select **Add a new row** action.

<img src="./media/be4f7a9c878d84b14b87e3c3288b35690b275f62.png"
style="width:6.26806in;height:2.74931in" />

11. Choose **Refund Requests** for the table name.

<img src="./media/eb81e1c4ae0a5b50469b573dcfff904dd6c0e6d1.png"
style="width:6.26806in;height:2.75417in" />

12. Select **Show all** to see all available fields.

<img src="./media/08c99792704777ec65c8dbaf6b7f64ab5eb7a34f.png"
style="width:6.26806in;height:2.73889in" />

13. Use **Dynamic content** to map each input parameter to the
    corresponding field:

    1.  **Name** Dynamic Input → **Full Name** Parameter.

    2.  **Purchase Date** Dynamic Input → **Date of Purchase**
        Parameter.

    3.  **Description** Dynamic Input → **Description** Parameter.

    4.  **Email** Dynamic Input → **Email** Parameter.

    5.  **Order Number** Dynamic Input → **Order Number** Parameter.

    6.  **Order Type** Dynamic Input → **Order Type** Parameter.

    7.  **Phone Number** Dynamic Input → **Phone Number** Parameter.

    8.  **Product** Dynamic Input → **Product** Parameter.

    9.  **Receipt Number** Dynamic Input → **Receipt Number** Parameter.

    10. **Contact Method** Dynamic Input → **Preferred Contact Method**
        Parameter.

> <img src="./media/2e3b70b6a3c97e03858c95403692a211675f10ea.png"
> style="width:6.26806in;height:2.72917in" />
>
> <img src="./media/07d0b8c419e633c50d8a95f819afd21f5dfd7d78.png"
> style="width:6.26806in;height:2.78542in" />

14. Select **Respond to Copilot** action.

15. Click on **Settings**.

16. Ensure that **Asynchronous Response** is set to **Off**.

> <img src="./media/54f7d8120c5012936caebb378847047380c9e81d.png"
> style="width:6.26806in;height:2.77361in" />

17. Select **Save draft**.

18. Then, click on **Publish**.

> <img src="./media/b1b442e6d8e9d47b886ce7a8663180edf3605082.png"
> style="width:6.26806in;height:2.96319in" />

19. Once the flow is published, close the Power Automate tab to return
    to Copilot Studio.

## Task 4: Create Action in Copilot for Refund Requests

1.  Go to copilot window and click on **Refresh**, (If the Copilot
    window was closed, reopen it and navigate back to the **Copilot
    Studio.** Go to the **Actions** tab and click on **+ Add an
    action**.)

<img src="./media/2bd1ef07e00f9caf9698cd1d0180c52ae2dcdda0.png"
style="width:6.26806in;height:2.97639in" />

2.  In the "Choose an action" window, select the **Refund Requests
    Flow** you created.

<img src="./media/7eafadf8d361ab040f159872170ae6e9d587d6e5.png"
style="width:6.26806in;height:2.97847in" />

3.  Click on **Next**, **Next** then **Next** again, and finally
    **Finish**. The flow will now be added as an action.

<img src="./media/3f194658afa3c7d9f4c3a0d94a38bbf546884977.png"
style="width:6.26806in;height:2.93125in" />

<img src="./media/0615b47f0b03c179303f6f3b2114361da150803e.png"
style="width:6.26806in;height:2.92431in" />

<img src="./media/c5079e5ba391f624d73f02ca9e0d94c4522e33e3.png"
style="width:6.26806in;height:2.88264in" />

4.  Navigate to the **Topics** section.

5.  Select the **Refund Requests** topic.

<img src="./media/258000b632042ce0c5e948728fd91cd620906b85.png"
style="width:6.26806in;height:2.96042in" />

6.  Below the Adaptive Card node, click on the **+** sign to create a
    new node.

7.  Select **Call an action**.

8.  Choose the **Refund Requests Flow**. This action will now be added
    below the Adaptive Card node.

<img src="./media/03c7c488d1d645430d98860461364d148a7837a8.png"
style="width:6.26806in;height:3.0375in" />

9.  In the action node, you need to map each input field to the
    appropriate variable created by the Adaptive Card:

    1.  **Name** Input: Click on the input field, then select
        **fullname** from the custom variables.

    2.  **Email** Input: Click on the input field, then select **email**
        from the custom variables.

    3.  **Phone Number** Input: Click on the input field, then select
        **phoneNumber** from the custom variables.

    4.  **Product** Input: Click on the input field, then select
        **product** from the custom variables.

    5.  **Contact Method** Input: Click on the input field, then select
        **contactMethod** from the custom variables.

    6.  **Order Type** Input: Click on the input field, then select
        **orderType** from the custom variables.

    7.  **Receipt Number** Input: Click on the input field, then select
        **receiptNumber** from the custom variables.

    8.  **Order Number** Input: Click on the input field, then select
        **orderNumber** from the custom variables.

    9.  **Purchase Date** Input: Click on the input field, then select
        **purchaseDate** from the custom variables.

    10. **Description** Input: Click on the input field, then select
        **description** from the custom variables.

> <img src="./media/8dcdde06b4508b0af7962a24e0ade05bbef55861.png"
> style="width:6.26806in;height:2.91528in" />
>
> <img src="./media/03e1ddb2ecaa171b45564f89311a0df18a6d099f.png"
> style="width:6.26806in;height:2.97708in" />

10. After mapping all the variables, click on the **Save** button to
    save the topic configuration.

<img src="./media/367e5011b84718323975c9556971f659b7873dcd.png"
style="width:6.26806in;height:2.96528in" />

## Task 5: Publish Your Copilot

1.  Navigate to Overview section and In Microsoft Copilot Studio, look
    for the **Publish** button on the right side of the screen.

2.  Click on the **Publish** button to start the publishing process.

<img src="./media/ea792bcf25b77cb284c82020057a9d6a8f06ce5e.png"
style="width:6.26806in;height:2.95764in" />

3.  A confirmation dialog may appear. Select **Publish** again to
    finalize and publish your copilot.

<img src="./media/56c6e3b03e4219bf44c4d39beead2b0ecdd46080.png"
style="width:6.26806in;height:2.97292in" />

## Conclusion

After completing this exercise, you have gained the following knowledge:

1.  You designed a Power Automate flow to capture appointment details
    and store them in Dataverse. This flow was then integrated into the
    Copilot to enable users to book appointments seamlessly.

2.  You created a separate Power Automate flow for processing refund
    requests. This flow also captured detailed user inputs and recorded
    them in Dataverse, integrating the flow into the Copilot for
    efficient refund management.

These automated workflows enhance the Copilot's functionality, allowing
it to handle appointments and refunds effectively, improving overall
user experience.

# Test Your Copilot

To test the functionalities of your Copilot and Power Automate flows,
follow these steps:

1.  Click on the three-dot right side of the window and select **Go to
    demo website.** A demo website window will open start the
    conversation into the website chat window.

<img src="./media/889ffefecee6e7b9abcb7e320c93b856197b59d5.png"
style="width:6.26806in;height:2.92778in" />

<img src="./media/bb5ba9165f4b24071ea669dbe3f94b8cff1c8460.png"
style="width:6.26806in;height:2.96042in" />

2.  Enter the following trigger phrases for information about the laptop
    and book appointment to test:

<!-- -->

1.  What are some deals on student laptops right now?

<img src="./media/457dc7bf04abe851ddca6d3c13828859708c3de2.png"
style="width:6.26806in;height:2.80208in" />

<img src="./media/af451526a0599e4552c94adaec800523098e6b8f.png"
style="width:6.26806in;height:2.96875in" />

2.  Tell me more about Surface Laptop Go 3. What are the specs & cost?

> <img src="./media/ff2da8cc5390d23dd3a13541968fd622f1ebf4bc.png"
> style="width:6.26806in;height:2.96389in" />
>
> <img src="./media/a7f6070fe603cd44f1d3b21a833e2c74aca0a4ba.png"
> style="width:6.26806in;height:2.95208in" />

3.  Compare laptop surface laptop pro 3 and surface laptop studio 2.

> <img src="./media/6bfa5731246412d23170f118e850cb3ab35b19b8.png"
> style="width:6.26806in;height:2.97917in" />
>
> <img src="./media/ee3e1faf59fb60c75a910e61977bd4acd839abaa.png"
> style="width:6.26806in;height:2.94792in" />

4.  Book Appointment for further assistance

> <img src="./media/6ea45028b6e077f842b114d66d01702bfe5a9e5e.png"
> style="width:6.26806in;height:2.97361in" />
>
> <img src="./media/d1db775af364106047c32d3506cc450d7cefa49c.png"
> style="width:6.26806in;height:2.96736in" />

5.  Ensure that the details entered in the Appointment Booking are
    accurately reflected in the "Book Appointments" table in Power Apps.

> <img src="./media/a7aca95ffa82eea0dc2d15d04cac1628b19feb3f.png"
> style="width:6.26806in;height:2.96042in" />

3.  Enter the following trigger phrases to test the topics you created:

    1.  I want to know about the Contoso refund policy.

<img src="./media/eab1032c1b79fdb4d6590fc627aad9ed6021302b.png"
style="width:6.26806in;height:2.95208in" />

<img src="./media/926b1347a5989f7d9f151365847fb4834ff4a68b.png"
style="width:6.26806in;height:2.95556in" />

2.  I buy laptop 10 days ago, is I eligible to return laptop.

<img src="./media/036f73372b5206b43805e46759039818064e7847.png"
style="width:6.26806in;height:2.93125in" />

<img src="./media/2a515176c275a11a5558d77f687c181fa4adb2ae.png"
style="width:6.26806in;height:2.96389in" />

3.  I buy laptop 3 day ago; I have to submit refund request.

<img src="./media/0b163b593ecce4c3051bbba2bd97b5318b57f46d.png"
style="width:6.26806in;height:2.94236in" />

<img src="./media/6c86d7588a4b92fad34c969ff58cda899a9b16f2.png"
style="width:6.26806in;height:2.82222in" />

4.  Ensure that the details entered in the Appointment Booking are
    accurately reflected in the "Refund Requests" table in Power Apps.

<img src="./media/c146d6a20ac4d8b5d0ec16cbb728c57405760259.png"
style="width:6.26806in;height:2.96458in" />

# Final Conclusion

In conclusion, the steps taken in setting up Dynamics 365 Customer
Service, enrolling in Microsoft Power Apps and Copilot Studio, and
creating custom tables have established a solid foundation for effective
and streamlined operations.

1.  **Dynamics 365 Customer Service Setup:** We signed up for a trial,
    managed users, and configured essential settings, laying the
    foundation for optimized customer service operations.

2.  **Microsoft Power Apps and Copilot Studio Enrolment:** We signed up
    for both platforms, setting up our accounts and environments to
    start building and integrating automated solutions.

3.  **Custom Table Creation in Power Apps:** We created and configured
    custom tables—"Book Appointments" and "Refund Requests"—to manage
    and organize data effectively, ensuring that all necessary
    information is captured.

4.  **Copilot Configuration in Microsoft Copilot Studio:** We set up a
    new copilot for Contoso Electronics, including naming it,
    configuring security settings, enabling AI features, cleaning up
    sample topics, creating a knowledge base, and publishing it for
    operational use.

5.  **Topic Management in Copilot Studio:** We developed various topics
    to handle customer inquiries, such as "Product Information," "Return
    Policy Information," and others. We also fine-tuned settings for
    effective customer interaction.

6.  **Integration of Power Automate Flows:** We created and integrated
    Power Automate flows to automate key processes like booking
    appointments and handling refund requests, enhancing our copilot’s
    functionality and user experience.
