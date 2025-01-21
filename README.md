# IO.Swagger - the C# library for the Revenium Metering API

Revenium Metering API

This C# SDK is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.14.0-SNAPSHOT
- SDK version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.dotnet.CSharpClientCodegen
    For more information, please visit [https://revenium.io](https://revenium.io)

<a name="frameworks-supported"></a>
## Frameworks supported
- .NET 4.0 or later
- Windows Phone 7.1 (Mango)

<a name="dependencies"></a>
## Dependencies
- [RestSharp](https://www.nuget.org/packages/RestSharp) - 105.1.0 or later
- [Json.NET](https://www.nuget.org/packages/Newtonsoft.Json/) - 7.0.0 or later
- [JsonSubTypes](https://www.nuget.org/packages/JsonSubTypes/) - 1.2.0 or later

The DLLs included in the package may not be the latest version. We recommend using [NuGet](https://docs.nuget.org/consume/installing-nuget) to obtain the latest version of the packages:
```
Install-Package RestSharp
Install-Package Newtonsoft.Json
Install-Package JsonSubTypes
```

NOTE: RestSharp versions greater than 105.1.0 have a bug which causes file uploads to fail. See [RestSharp#742](https://github.com/restsharp/RestSharp/issues/742)

<a name="installation"></a>
## Installation
Run the following command to generate the DLL
- [Mac/Linux] `/bin/sh build.sh`
- [Windows] `build.bat`

Then include the DLL (under the `bin` folder) in the C# project, and use the namespaces:
```csharp
using IO.Swagger.io.revenium;
using IO.Swagger.Client;
using IO.Swagger.io.revenium;
```
<a name="packaging"></a>
## Packaging

A `.nuspec` is included with the project. You can follow the Nuget quickstart to [create](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package#create-the-package) and [publish](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package#publish-the-package) packages.

This `.nuspec` uses placeholders from the `.csproj`, so build the `.csproj` directly:

```
nuget pack -Build -OutputDirectory out IO.Swagger.csproj
```

Then, publish to a [local feed](https://docs.microsoft.com/en-us/nuget/hosting-packages/local-feeds) or [other host](https://docs.microsoft.com/en-us/nuget/hosting-packages/overview) and consume the new package via Nuget as usual.

<a name="getting-started"></a>
## Getting Started

```csharp
using System;
using System.Diagnostics;
using IO.Swagger.io.revenium;
using IO.Swagger.Client;
using IO.Swagger.io.revenium;

namespace Example
{
    public class Example
    {
        public void main()
        {
            var apiInstance = new EventsApi();
            var body = new ApiEventDTO(); // ApiEventDTO | 

            try
            {
                // Save can API event
                apiInstance.SaveEvent(body);
            }
            catch (Exception e)
            {
                Debug.Print("Exception when calling EventsApi.SaveEvent: " + e.Message );
            }
        }
    }
}
```

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *https://api.revenium.io/meter/v1/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*EventsApi* | [**SaveEvent**](docs/EventsApi.md#saveevent) | **POST** /event | Save can API event
*MeteringApi* | [**Meter**](docs/MeteringApi.md#meter) | **POST** /meter | Insert API metering data
*MeteringApi* | [**Valid**](docs/MeteringApi.md#valid) | **GET** /meter/product-key | Determine if a ProductKey is valid or not

<a name="documentation-for-models"></a>
## Documentation for Models

 - [io.revenium.ApiEventDTO](docs/ApiEventDTO.md)
 - [io.revenium.ElementDTO](docs/ElementDTO.md)
 - [io.revenium.MeteringRequestDTO](docs/MeteringRequestDTO.md)
 - [io.revenium.Unit](docs/Unit.md)

<a name="documentation-for-authorization"></a>
## Documentation for Authorization

<a name="x-api-key"></a>
### x-api-key

- **Type**: API key
- **API key parameter name**: x-api-key
- **Location**: HTTP header

