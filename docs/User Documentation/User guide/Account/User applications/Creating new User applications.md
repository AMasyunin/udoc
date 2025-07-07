
[Account](..\..\Account.md) > [User applications](..\User%20applications.md)

# Creating new User applications

When setting up a new **User application**, you'll work with several key configurations that determine how your external application integrates with the platform. Let's explore each essential component.

Start by clicking the ![chrome_py0qhiu5p8.webp](..\..\..\attachments\0f178ad6-466d-4126-b5d8-666565ebff79.webp) button in the **User applications** list. In the appeared configuration form, proceed with the following steps:

### 1. Set up the URL

Specify your application URL - the address where your application is hosted, it serves as the foundation for the integration.

> [!IMPORTANT]
> **Important**
>
> - Ensure the URL is valid, uses an HTTPS connection, leads to a trustworthy resource, and contains no more than 1000 characters.
> - Make sure the application has the iFrame setting enabled on its side, otherwise you will not be able to open it in the platform interface.

### 2. Configure basic Parameters

To personalize your application, you can include various parameters in the URL. You can manually add parameters in the URL field or use one of our suggestions: language, user ID, or time zone. Click on a parameter suggestion to add it to the end of the URL. Expand the description below to learn more about the suggested parameters and examples.

<details>
<summary>Understanding suggested URL parameters</summary>

We suggest some basic parameters for personalization

1. `?locale={locale_code}`  
   Language parameter that automatically matches the user's platform language.

   - Example: `https://your-app.com/dashboard?locale=en`
2. `?user_id={user_identifier}`  
   User context parameter that passes user identity to filter personalized information.

   - Example: `https://your-app.com/dashboard?user_id=12345`
3. `?timezone={timezone}`  
   Time parameter that automatically matches the user’s platform time zone.

   - Example: `https://your-app.com/dashboard?timezone=UTC+1`

You can edit the suggested parameter name or specify a certain value for it.

</details>

![URL_with_Params.png](..\..\..\attachments\4a46a901-9551-4d61-b3a7-7041dc29e13c.png)
> [!NOTE]
> Test your configuration to make sure the application loads correctly. Click ![image-20241217-083119.png](..\..\..\attachments\ef0010ac-2759-434a-b424-68aeed474e28.png) to display a preview.

### 3. Adjust appearance

Create a recognizable identity for your application to make it easy to access. The following settings will help you to do so:

- **Label** – Add a unique, descriptive name for your app (up to 24 characters). It will be shown in the platform sidebar.
- **Description** – Add a brief explanation with details about the app’s functionality or highlight important information (up to 50 characters). An informative description will help your users to get a clearer understanding of the app’s purpose.
- **Icon** – Select an icon that represents your application's function for even more native navigation.

### 4. Select display method

Decide how your application will open by choosing one of the two options in the **Open in** dropdown:

- **Embedded** – App appears within the platform interface
- **New tab** – App opens in a separate browser tab

> [!NOTE]
> Our platform uses iFrame for embedding. Since not all URLs can be successfully processed with this technology, be sure to preview the embedding result. If you encounter any issues with this display method, please consider using **New tab**.

### 5. Set up authentication (optional)

Configure authentication if your application relies on the platform’s API. In this case, the platform will provide the authentication data directly to the application when it is opened, eliminating the need to implement additional login functionality on your application side.  
You can choose one of the two authentication methods:

- **API key**

  - This method is for applications where role management or user permissions are not required.
  - The API key corresponds to the account owner’s access level. This means providing a common user with an API key may grant them access to **all data** available to the main user.  
    For example, if your application works with trackers to which a user has limited rights or no access at all, using the API key will still expose all trackers from the main account.
- **Session key**

  - This method is recommended when role management is involved.
  - Transmits the current user session key to the application.

> [!NOTE]
> Selecting the **API key** method will automatically disable the **Session key** method, and vice versa. Only one method can be used at a time.

When authentication is enabled, the platform appends the `?session_key=` parameter to your application’s URL.

- If you’ve selected an **API key**, the parameter’s value will contain this key.
- If you’ve opted for a **Session key**, the parameter value will include the key of the current user session from which the application is being accessed.

Make sure the application is capable of reading and using this parameter.

### 6. Save the new application

Click the **Save** button. Your application will appear in the **User applications** list and the platform sidebar. Enabled applications automatically become available to the account users.

![](..\..\..\attachments\7f821c4f-96df-413d-b5af-1428e908a16d.png)
<details>
<summary>Quick troubleshooting tips</summary>

If your application doesn't display properly when embedded, try:

- Opening it in a new tab instead
- Verifying your URL is correct and accessible
- Checking that all parameters are properly formatted

</details>

The created applications remain fully configurable after they are saved. You can adjust their parameters and appearance at any time. To learn more about application management, see [Managing existing User applications](Managing existing User applications.md).
