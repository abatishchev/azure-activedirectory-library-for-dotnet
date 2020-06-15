---

This library, ADAL for .NET, will no longer receive new feature improvements. Instead, use the new library
[MSAL for .NET](https://github.com/AzureAD/microsoft-authentication-library-for-dotnet).

* If you are starting a new project, you can get started with the
  [MSAL for .NET docs](https://github.com/AzureAD/microsoft-authentication-library-for-dotnet/wiki)
  for details about the scenarios, usage, and relevant concepts.
* If your application is using the previous ADAL for .NET library, you can follow this
  [migration guide for .NET apps](https://docs.microsoft.com/en-us/azure/active-directory/develop/msal-net-migration), this [migration guide for brokered iOS Xamarin apps](https://docs.microsoft.com/en-us/azure/active-directory/develop/msal-net-migration-ios-broker), or this [migration guide for brokered Android Xamarin apps](https://github.com/AzureAD/microsoft-authentication-library-for-dotnet/wiki/How-to-migrate-from-using-Android-Broker-on-ADAL.NET-to-MSAL.NET).
* Existing applications relying on ADAL for .NET will continue to work.

---

# Active Directory Authentication Library (ADAL) for .NET, Windows Store, .NET Core, Xamarin iOS and Xamarin Android

| [Conceptual documentation](https://github.com/AzureAD/azure-activedirectory-library-for-dotnet/wiki#documentation) | [Code Samples](https://github.com/azure-samples?utf8=✓&q=active-directory-dotnet) | [Reference Docs](https://docs.microsoft.com/active-directory/adal/microsoft.identitymodel.clients.activedirectory) | [Developer Guide](https://aka.ms/aaddev) | [API Reference](https://docs.microsoft.com/en-us/dotnet/api/microsoft.identitymodel.clients.activedirectory?view=azure-dotnet) |
| ------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |

## Update to MSAL.NET now!

[MSAL.NET](https://github.com/AzureAD/microsoft-authentication-library-for-dotnet) is the new authentication library to be used with the Microsoft identity platform

Building on top of ADAL, MSAL works with the new and Open ID Connect certified Azure AD V2 endpoint and the new social identity solution from Microsoft, Azure AD B2C.

ADAL.NET is in maintenance mode and no new features will be added to ADAL.NET anymore. All our ongoing efforts will be focused on improving the new [MSAL.NET](https://github.com/AzureAD/microsoft-authentication-library-for-dotnet). MSAL’s documentation also contains a [migration guide]( https://docs.microsoft.com/en-us/azure/active-directory/develop/msal-net-migration) which simplifies upgrading from ADAL.NET, including how to migrate Xamarin.iOS apps using brokers.

## ADAL.NET 2.x is no longer supported

ADAL.NET 2.x is no longer supported. ADAL.NET 3.x became generally available more than 3 years ago, superseding ADAL 2.x which was last released in August 2017
If you are still using 2.x, we recommend that you update directly to MSAL.NET

## ADAL.NET

Active Directory Authentication Library for .NET (ADAL.NET) is an easy to use authentication library. You can use ADAL.NET to acquire **security tokens to access protected Web APIs**, for instance Microsoft Graph, or another Web APIs. ADAL.NET is available on various .NET Desktop/Mobile platforms to acquire a token for the signed-in user ( Windows desktop, UWP, Windows 8.1, Xamarin iOS and Xamarin Android). It can also be used in Web applications and Web APIs (ASP.NET, .NET Core, ASP.NET Core) that call other Web APIs in the name of a user, or without a user. ADAL.NET takes advantage of Windows Server Active Directory and Windows Azure Active Directory.

| Release | Location                                                                                                                                                                                                      |
| ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Stable  | [![NuGet](https://img.shields.io/nuget/v/Microsoft.IdentityModel.Clients.ActiveDirectory.svg?style=flat-square&label=nuget)](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/) |

## Build status

| dev                                                                                                                                                                                                                                  | adalV3/dev                                                                                                                                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [![Build status](https://identitydivision.visualstudio.com/_apis/public/build/definitions/a7934fdd-dcde-4492-a406-7fad6ac00e17/556/badge)](https://identitydivision.visualstudio.com/IDDP/IDDP%20Team/_build/index?definitionId=556) | [![Build status](https://identitydivision.visualstudio.com/_apis/public/build/definitions/a7934fdd-dcde-4492-a406-7fad6ac00e17/187/badge)](https://identitydivision.visualstudio.com/IDDP/IDDP%20Team/_build/index?definitionId=187) |

## Branches

**dev**: Contains newest development of ADAL (v4+)
**adalV3/dev** : Holds the v3 branch. Only security fixes will make it to v3.

## Versions

Current version - latest one at [nuget.org](https://www.nuget.org/packages/Microsoft.IdentityModel.Clients.ActiveDirectory/).  
Minimum recommended version - 3.19.8

You can find the changes for each version in the [change log](https://github.com/AzureAD/azure-activedirectory-library-for-dotnet/blob/master/changelog.txt).

## Security Issue in Multiple Versions of ADAL .Net

A defect in ADAL .Net can result in an elevation of privilege in specific problem scenarios. The problem scenarios involve the On Behalf Of protocol flow and specific use cases of a ClientAssertion/ClientAssertionCertificate/ClientCredential and UserAssertion being passed to the AcquireToken* API. Multiple versions of the library are affected. Affected versions are listed below.

We have emailed owners of active applications that are using an impacted version of the library in the specific problem scenarios.

The latest stable version of the library does not have the defect. To avoid being impacted we strongly recommend you update to at least 2.28.1 for 2.x, 3.13.4 for 3.x, or the latest stable version. If you have questions about this issue, please email aadintegrate@microsoft.com.

Affected 2.x versions: 2.27.306291202, 2.26.305102204, 2.26.305100852, 2.25.305061457, 2.21.301221612, 2.20.301151232, 2.19.208020213, 2.18.206251556, 2.17.206230854, 2.16.204221202, 2.15.204151539, 2.14.201151115, 2.13.112191810, 2.12.111071459, 2.11.10918.1222, 2.10.10910.1511, 2.9.10826.1824, 2.8.10804.1442-rc, 2.7.10707.1513-rc, 2.6.2-alpha, 2.6.1-alpha, 2.5.1-alpha

Affected 3.x versions: 3.11.305310302-alpha, 3.10.305231913, 3.10.305161347, 3.10.305110106, 3.5.208051316-alpha, 3.5.208012240-alpha, 3.5.207081303-alpha, 3.4.206191646-alpha, 3.3.205061641-alpha, 3.2.204281119-alpha, 3.1.203031538-alpha, 3.0.110281957-alpha

## Samples and Documentation

We provide a full suite of [sample applications](https://github.com/Azure-Samples?utf8=%E2%9C%93&q=active-directory) and [ADAL documentation](https://docs.microsoft.com/active-directory/adal/microsoft.identitymodel.clients.activedirectory) to help you get started with learning the Azure Identity system. Our [Azure AD Developer Guide](https://aka.ms/aaddev) includes tutorials for native clients such as Windows, Windows Phone, iOS, OSX, Android, and Linux. We also provide full walkthroughs for authentication flows such as OAuth2, OpenID Connect, Graph API, and other awesome features.

## Community Help and Support

We leverage [Stack Overflow](http://stackoverflow.com/) to work with the community on supporting Azure Active Directory and its SDKs, including this one! We highly recommend you ask your questions on Stack Overflow (we're all on there!) Also browser existing issues to see if someone has had your question before.

We recommend you use the "adal" tag so we can see it! Here is the latest Q&A on Stack Overflow for ADAL: [http://stackoverflow.com/questions/tagged/adal](http://stackoverflow.com/questions/tagged/adal)

## Security Reporting

If you find a security issue with our libraries or services please report it to [secure@microsoft.com](mailto:secure@microsoft.com) with as much detail as possible. Your submission may be eligible for a bounty through the [Microsoft Bounty](http://aka.ms/bugbounty) program. Please do not post security issues to GitHub Issues or any other public site. We will contact you shortly upon receiving the information. We encourage you to get notifications of when security incidents occur by visiting [this page](https://technet.microsoft.com/en-us/security/dd252948) and subscribing to Security Advisory Alerts.

## Contributing

All code is licensed under the MIT license and we triage actively on GitHub. We enthusiastically welcome contributions and feedback. You can clone the repo and start contributing now, but check [this document](./contributing.md) first.

## Diagnostics

The following are the primary sources of information for diagnosing issues:

+ Exceptions
+ Logs
+ Network traces

Also, note that correlation IDs are central to the diagnostics in the library.  You can set your correlation IDs on a per request basis (by setting `CorrelationId` property on `AuthenticationContext` before calling an acquire token method) if you want to correlate an ADAL request with other operations in your code. If you don't set a correlations id, then ADAL will generate a random one which changes on each request. All log messages and network calls will be stamped with the correlation id.  

### Exceptions

This is obviously the first diagnostic.  We try to provide helpful error messages.  If you find one that is not helpful please file an [issue](https://github.com/AzureAD/azure-activedirectory-library-for-dotnet/issues) and let us know. Please also provide the target platform of your application (e.g. Desktop, Windows Store, Windows Phone).

### Logs

In order to configure logging, see the [wiki](https://github.com/AzureAD/azure-activedirectory-library-for-dotnet/wiki/Logging-in-ADAL.Net) page for implementation details.

### Using brokers

See [Leveraging brokers on Android and iOS](https://github.com/AzureAD/azure-activedirectory-library-for-dotnet/wiki/leveraging-brokers-on-Android-and-iOS)

### Network Traces

You can use various tools to capture the HTTP traffic that ADAL generates.  This is most useful if you are familiar with the OAuth protocol or if you need to provide diagnostic information to Microsoft or other support channels.

Fiddler is the easiest HTTP tracing tool.  In order to be useful it is necessary to configure fiddler to record unencrypted SSL traffic.  

NOTE: Traces generated in this way may contain highly privileged information such as access tokens, usernames and passwords.  If you are using production accounts, do not share these traces with 3rd parties.  If you need to supply a trace to someone in order to get support, reproduce the issue with a temporary account with usernames and passwords that you don't mind sharing.

## License

Copyright (c) Microsoft Corporation.  All rights reserved. Licensed under the MIT License (the "License");

## We Value and Adhere to the Microsoft Open Source Code of Conduct

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
