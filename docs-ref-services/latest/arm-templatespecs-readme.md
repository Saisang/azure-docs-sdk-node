---
title: Azure TemplateSpecs client library for JavaScript
keywords: Azure, javascript, SDK, API, @azure/arm-templatespecs, templatespecs
author: qiaozha
ms.author: qiaozha
ms.date: 12/16/2021
ms.topic: reference
ms.prod: azure
ms.technology: azure
ms.devlang: javascript
ms.service: templatespecs
---
# Azure TemplateSpecs client library for JavaScript - Version 2.0.0 


This package contains an isomorphic SDK (runs both in Node.js and in browsers) for Azure TemplateSpecs client.

The APIs listed in this specification can be used to manage Template Spec resources through the Azure Resource Manager.

[Source code](https://github.com/Azure/azure-sdk-for-js/tree/@azure/arm-templatespecs_2.0.0/sdk/templatespecs/arm-templatespecs) |
[Package (NPM)](https://www.npmjs.com/package/@azure/arm-templatespecs) |
[API reference documentation](https://docs.microsoft.com/javascript/api/@azure/arm-templatespecs) |
[Samples](https://github.com/Azure-Samples/azure-samples-js-management)

## Getting started

### Currently supported environments

- [LTS versions of Node.js](https://nodejs.org/about/releases/)
- Latest versions of Safari, Chrome, Edge and Firefox.

### Prerequisites

- An [Azure subscription][azure_sub].

### Install the `@azure/arm-templatespecs` package

Install the Azure TemplateSpecs client library for JavaScript with `npm`:

```bash
npm install @azure/arm-templatespecs
```

### Create and authenticate a `TemplateSpecsClient`

To create a client object to access the Azure TemplateSpecs API, you will need the `endpoint` of your Azure TemplateSpecs resource and a `credential`. The Azure TemplateSpecs client can use Azure Active Directory credentials to authenticate.
You can find the endpoint for your Azure TemplateSpecs resource in the [Azure Portal][azure_portal].

You can authenticate with Azure Active Directory using a credential from the [@azure/identity][azure_identity] library or [an existing AAD Token](https://github.com/Azure/azure-sdk-for-js/blob/@azure/arm-templatespecs_2.0.0/sdk/identity/identity/samples/AzureIdentityExamples.md#authenticating-with-a-pre-fetched-access-token).

To use the [DefaultAzureCredential][defaultazurecredential] provider shown below, or other credential providers provided with the Azure SDK, please install the `@azure/identity` package:

```bash
npm install @azure/identity
```

You will also need to **register a new AAD application and grant access to Azure TemplateSpecs** by assigning the suitable role to your service principal (note: roles such as `"Owner"` will not grant the necessary permissions).
Set the values of the client ID, tenant ID, and client secret of the AAD application as environment variables: `AZURE_CLIENT_ID`, `AZURE_TENANT_ID`, `AZURE_CLIENT_SECRET`.

For more information about how to create an Azure AD Application check out [this guide](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal).

```javascript
const { TemplateSpecsClient } = require("@azure/arm-templatespecs");
const { DefaultAzureCredential } = require("@azure/identity");
const subscriptionId = "00000000-0000-0000-0000-000000000000";
const client = new TemplateSpecsClient(new DefaultAzureCredential(), subscriptionId);
```


### JavaScript Bundle
To use this client library in the browser, first you need to use a bundler. For details on how to do this, please refer to our [bundling documentation](https://aka.ms/AzureSDKBundling).

## Key concepts

### TemplateSpecsClient

`TemplateSpecsClient` is the primary interface for developers using the Azure TemplateSpecs client library. Explore the methods on this client object to understand the different features of the Azure TemplateSpecs service that you can access.

## Troubleshooting

### Logging

Enabling logging may help uncover useful information about failures. In order to see a log of HTTP requests and responses, set the `AZURE_LOG_LEVEL` environment variable to `info`. Alternatively, logging can be enabled at runtime by calling `setLogLevel` in the `@azure/logger`:

```javascript
const { setLogLevel } = require("@azure/logger");
setLogLevel("info");
```

For more detailed instructions on how to enable logs, you can look at the [@azure/logger package docs](https://github.com/Azure/azure-sdk-for-js/tree/@azure/arm-templatespecs_2.0.0/sdk/core/logger).

## Next steps

Please take a look at the [samples](https://github.com/Azure-Samples/azure-samples-js-management) directory for detailed examples on how to use this library.

## Contributing

If you'd like to contribute to this library, please read the [contributing guide](https://github.com/Azure/azure-sdk-for-js/blob/@azure/arm-templatespecs_2.0.0/CONTRIBUTING.md) to learn more about how to build and test the code.

## Related projects

- [Microsoft Azure SDK for JavaScript](https://github.com/Azure/azure-sdk-for-js)

![Impressions](https://azure-sdk-impressions.azurewebsites.net/api/impressions/azure-sdk-for-js%2Fsdk%2Ftemplatespecs%2Farm-templatespecs%2FREADME.png)

[azure_cli]: https://docs.microsoft.com/cli/azure
[azure_sub]: https://azure.microsoft.com/free/
[azure_sub]: https://azure.microsoft.com/free/
[azure_portal]: https://portal.azure.com
[azure_identity]: https://github.com/Azure/azure-sdk-for-js/tree/@azure/arm-templatespecs_2.0.0/sdk/identity/identity
[defaultazurecredential]: https://github.com/Azure/azure-sdk-for-js/tree/@azure/arm-templatespecs_2.0.0/sdk/identity/identity#defaultazurecredential
