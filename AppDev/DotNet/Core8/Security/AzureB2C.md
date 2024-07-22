Complete B2C Tutorial
https://learn.microsoft.com/en-us/azure/active-directory-b2c/

1. Register application on Azure Domain


OpenID Connect (OIDC) is an authentication protocol that's built on OAuth 2.0. 

Microsoft Identity Web is a set of ASP.NET Core libraries that simplify adding authentication and authorization support to web apps.


Config Parameters

```json
  "AzureAdB2C": {
    //"Instance": "https://fabrikamb2c.b2clogin.com",
    "Instance": "https://t360modernization.b2clogin.com",
    //"ClientId": "90c0fe63-bcf2-44d5-8fb7-b8bbc0b29dc6",
    "ClientId": "f88be67e-9369-4a1a-9bc5-304c03ebe083",
    //"Domain": "fabrikamb2c.onmicrosoft.com",
    "Domain": "t360modernization.onmicrosoft.com",
    "SignedOutCallbackPath": "/signout/B2C_1_Defi_SignInUp",

    "SignUpSignInPolicyId": "B2C_1_Defi_SignInUp",
    "ResetPasswordPolicyId": "B2C_1_Defi_PwdReset",
    "EditProfilePolicyId": "B2C_1_Defi_EditProfile" // Optional profile editing policy
    //"CallbackPath": "/signin/B2C_1_sign_up_in"  // defaults to /signin-oidc
  },
```

Configure for MVC App
https://learn.microsoft.com/en-us/azure/active-directory-b2c/enable-authentication-web-application

https://learn.microsoft.com/en-us/azure/active-directory-b2c/enable-authentication-web-application-options

Configure Azure for B2C App
1. 
https://learn.microsoft.com/en-us/azure/active-directory-b2c/tutorial-create-tenant


Configure for Blazor or SPA
https://learn.microsoft.com/en-us/aspnet/core/blazor/security/webassembly/hosted-with-azure-active-directory-b2c?view=aspnetcore-7.0&viewFallbackFrom=aspnetcore-8.0


dotnet new blazorwasm -au IndividualB2C --aad-b2c-instance "{AAD B2C INSTANCE}" --api-client-id "f88be67e-9369-4a1a-9bc5-304c03ebe083" --app-id-uri "863978fc-5512-4f2e-a6d0-dcee2832e16e" --client-id "b739d752-634b-405d-b80a-c88c5a9e4546" --default-scope "API.Access" --domain "t360modernization.onmicrosoft.com" -ho -o BlazorSample -ssp "B2C_1_signupsignin_api"


https://learn.microsoft.com/en-us/azure/active-directory-b2c/configure-authentication-sample-spa-app#step-23-register-the-spa