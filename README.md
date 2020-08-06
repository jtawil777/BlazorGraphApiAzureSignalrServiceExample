# BlazorGraphApi

Blazor Server App with Azure AD Authentication, that calls the Microsoft Graph API on-behalf of the signed-in user.

This code uses [Microsoft.Indentity.Web](https://github.com/AzureAD/microsoft-identity-web)

You will need to register your app in Azure and modify appsettings.json to include your details

```
{
  "AzureAd": {
    "Instance": "https://login.microsoftonline.com/",
    "Domain": "your.domain",
    "TenantId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
    "ClientId": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
    "ClientSecret": "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx",
    "ClientCertificates": [
    ],
    "CallbackPath": "/signin-oidc"
  },
  "CalledApi": {
    "CalledApiScopes": "user.read",
    "CalledApiUrl": "https://graph.microsoft.com/beta"
  },
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft": "Warning",
      "Microsoft.Hosting.Lifetime": "Information"
    }
  },
  "AllowedHosts": "*"
}
```

# Notes

Code has now been updated to include the new features, especially written for Blazor Server in
[Microsoft.Indentity.Web](https://github.com/AzureAD/microsoft-identity-web)


This is a minimal example of calling MS Graph Api from Blazor Server.
Microsoft.Identity.Web contains many other features which can be used in Blazor Server, including calling downstream WebApi's and using incremental consent.

Hopefully these features will be rolled into the new project templates for Blazor in .NET 5


For more infor refer to [Microsoft.Indentity.Web](https://github.com/AzureAD/microsoft-identity-web)
