---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 5a9141cf0f609eedd35c25f6fd3d7977201e58c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246462"
---
# <span data-ttu-id="81370-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="81370-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="81370-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81370-102">SYNOPSIS</span></span>
<span data-ttu-id="81370-103">Импортирует API из файла или URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="81370-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="81370-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81370-104">SYNTAX</span></span>

### <span data-ttu-id="81370-105">ImportFromLocalFile (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="81370-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81370-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="81370-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81370-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81370-107">DESCRIPTION</span></span>
<span data-ttu-id="81370-108">Командлет **Import-AzApiManagementApi** импортирует API Azure API Management из файла или URL-адреса в языке описания веб-приложений (WADL), языка описания веб-служб (WSDL) или в формате Swagger.</span><span class="sxs-lookup"><span data-stu-id="81370-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="81370-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81370-109">EXAMPLES</span></span>

### <span data-ttu-id="81370-110">Пример 1: импорт API из файла WADL</span><span class="sxs-lookup"><span data-stu-id="81370-110">Example 1: Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="81370-111">Эта команда импортирует API из указанного файла WADL.</span><span class="sxs-lookup"><span data-stu-id="81370-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="81370-112">Пример 2: импорт API из файла Swagger</span><span class="sxs-lookup"><span data-stu-id="81370-112">Example 2: Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="81370-113">Эта команда импортирует API из указанного файла Swagger.</span><span class="sxs-lookup"><span data-stu-id="81370-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="81370-114">Пример 3: импорт API-интерфейса из ссылки WADL</span><span class="sxs-lookup"><span data-stu-id="81370-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="81370-115">Эта команда импортирует API из указанной ссылки WADL.</span><span class="sxs-lookup"><span data-stu-id="81370-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="81370-116">Пример 4: импорт API из ссылки Open API</span><span class="sxs-lookup"><span data-stu-id="81370-116">Example 4: Import an API from a Open Api Link</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationFormat OpenApi -SpecificationUrl https://raw.githubusercontent.com/OAI/OpenAPI-Specification/master/examples/v3.0/petstore.yaml -Path "petstore30"

ApiId                         : af3f57bab399455aa875d7050654e9d1
Name                          : Swagger Petstore
Description                   :
ServiceUrl                    : http://petstore.swagger.io/v1
Path                          : petstore30
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    :
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/af3f57bab399455aa875d7050654e9d1     
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="81370-117">Эта команда импортирует API-интерфейс из указанной ссылки на открытую спецификацию 3,0.</span><span class="sxs-lookup"><span data-stu-id="81370-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="81370-118">Пример 5: импорт API из ссылки Open API в набор ApiVersion</span><span class="sxs-lookup"><span data-stu-id="81370-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationPath "C:\contoso\specifications\uspto.yml" -SpecificationFormat OpenApi -Path uspostal -ApiVersionSetId 0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd -ApiVersion v2

ApiId                         : 6c3f20c66e5745b19229d06cd865948f
Name                          : USPTO Data Set API
Description                   : The Data Set API (DSAPI) allows the public users to discover and search USPTO exported data sets. This is a generic API that allows USPTO users to make any CSV based data files
                                searchable through API. With the help of GET call, it returns the list of data fields that are searchable. With the help of POST call, data can be fetched based on the filters on the    
                                field names. Please note that POST call is used to search the actual data. The reason for the POST call is that it allows users to specify any complex search criteria without worry      
                                about the GET size limitations as well as encoding of the input parameters.
ServiceUrl                    : https://developer.uspto.gov/ds-api
Path                          : uspostal
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v2
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd
Id                            : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis/6c3f20c66e5745b19229d06cd865948f    
ResourceGroupName             : Api-Default-East-US
ServiceName                   : contoso
```

<span data-ttu-id="81370-119">Эта команда импортирует API из указанного документа спецификации Open 3,0 и создает новый ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="81370-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="81370-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81370-120">PARAMETERS</span></span>

### <span data-ttu-id="81370-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="81370-121">-ApiId</span></span>
<span data-ttu-id="81370-122">Указывает идентификатор API для импорта.</span><span class="sxs-lookup"><span data-stu-id="81370-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="81370-123">Если этот параметр не указан, для вас создается идентификатор.</span><span class="sxs-lookup"><span data-stu-id="81370-123">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="81370-124">-ApiRevision</span></span>
<span data-ttu-id="81370-125">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="81370-125">Identifier of API Revision.</span></span> <span data-ttu-id="81370-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="81370-126">This parameter is optional.</span></span> <span data-ttu-id="81370-127">Если этот элемент не указан, импорт будет выполнен на текущую активную версию или в новый API-интерфейс.</span><span class="sxs-lookup"><span data-stu-id="81370-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-128">-ApiType</span><span class="sxs-lookup"><span data-stu-id="81370-128">-ApiType</span></span>
<span data-ttu-id="81370-129">Этот параметр является необязательным с использованием значения по умолчанию HTTP.</span><span class="sxs-lookup"><span data-stu-id="81370-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="81370-130">Параметр SOAP применим только при импорте WSDL и создаст API-интерфейс для протокола SOAP PassThrough.</span><span class="sxs-lookup"><span data-stu-id="81370-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="81370-131">-ApiVersion</span></span>
<span data-ttu-id="81370-132">Версия API создаваемого API-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="81370-132">Api Version of the Api to create.</span></span> <span data-ttu-id="81370-133">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="81370-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-134">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="81370-134">-ApiVersionSetId</span></span>
<span data-ttu-id="81370-135">Идентификатор ресурса для связанного набор версий API.</span><span class="sxs-lookup"><span data-stu-id="81370-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="81370-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="81370-136">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-137">-Context</span><span class="sxs-lookup"><span data-stu-id="81370-137">-Context</span></span>
<span data-ttu-id="81370-138">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="81370-138">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81370-139">-DefaultProfile</span></span>
<span data-ttu-id="81370-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81370-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81370-141">-Path</span><span class="sxs-lookup"><span data-stu-id="81370-141">-Path</span></span>
<span data-ttu-id="81370-142">Указывает путь веб-API как последнюю часть общедоступного URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="81370-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="81370-143">Этот URL-адрес используется клиентами API для отправки запросов на веб-службу.</span><span class="sxs-lookup"><span data-stu-id="81370-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="81370-144">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="81370-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="81370-145">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="81370-145">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-146">-Protocol (протокол)</span><span class="sxs-lookup"><span data-stu-id="81370-146">-Protocol</span></span>
<span data-ttu-id="81370-147">Протоколы веб-API (HTTP, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="81370-147">Web API protocols (http, https).</span></span> <span data-ttu-id="81370-148">Протоколы, через которые API станет доступным.</span><span class="sxs-lookup"><span data-stu-id="81370-148">Protocols over which API is made available.</span></span> <span data-ttu-id="81370-149">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="81370-149">This parameter is optional.</span></span> <span data-ttu-id="81370-150">При условии, что оно переопределит протоколы, указанные в документе спецификации.</span><span class="sxs-lookup"><span data-stu-id="81370-150">If provided it will override the protocols specified in the specifications document.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="81370-151">-ServiceUrl</span></span>
<span data-ttu-id="81370-152">URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="81370-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="81370-153">Этот URL-адрес будет использоваться только для управления API Azure и не будет открыт.</span><span class="sxs-lookup"><span data-stu-id="81370-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="81370-154">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="81370-154">This parameter is optional.</span></span> <span data-ttu-id="81370-155">Если оно задано, оно переопределяет ServiceUrl, указанный в документе "спецификации".</span><span class="sxs-lookup"><span data-stu-id="81370-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-156">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="81370-156">-SpecificationFormat</span></span>
<span data-ttu-id="81370-157">Задает формат спецификации.</span><span class="sxs-lookup"><span data-stu-id="81370-157">Specifies the specification format.</span></span>
<span data-ttu-id="81370-158">psdx_paramvalues WADL, WSDL и Swagger.</span><span class="sxs-lookup"><span data-stu-id="81370-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-159">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="81370-159">-SpecificationPath</span></span>
<span data-ttu-id="81370-160">Задает путь к файлу спецификации.</span><span class="sxs-lookup"><span data-stu-id="81370-160">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromLocalFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-161">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="81370-161">-SpecificationUrl</span></span>
<span data-ttu-id="81370-162">Указывает URL-адрес спецификации.</span><span class="sxs-lookup"><span data-stu-id="81370-162">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="81370-163">-WsdlEndpointName</span></span>
<span data-ttu-id="81370-164">Локальное имя конечной точки WSDL (порта), которое нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="81370-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="81370-165">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="81370-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="81370-166">Этот параметр является необязательным и требуется только для импорта WSDL.</span><span class="sxs-lookup"><span data-stu-id="81370-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="81370-167">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="81370-167">Default value is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-168">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="81370-168">-WsdlServiceName</span></span>
<span data-ttu-id="81370-169">Локальное имя службы WSDL, которую нужно импортировать.</span><span class="sxs-lookup"><span data-stu-id="81370-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="81370-170">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="81370-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="81370-171">Этот параметр является необязательным и требуется только для импорта WSDL.</span><span class="sxs-lookup"><span data-stu-id="81370-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="81370-172">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="81370-172">Default value is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81370-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81370-173">CommonParameters</span></span>
<span data-ttu-id="81370-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81370-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81370-175">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81370-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81370-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81370-176">INPUTS</span></span>

### <span data-ttu-id="81370-177">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="81370-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="81370-178">System. String</span><span class="sxs-lookup"><span data-stu-id="81370-178">System.String</span></span>

### <span data-ttu-id="81370-179">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="81370-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="81370-180">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementApiType, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="81370-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="81370-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81370-181">OUTPUTS</span></span>

### <span data-ttu-id="81370-182">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="81370-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="81370-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="81370-183">NOTES</span></span>

## <span data-ttu-id="81370-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81370-184">RELATED LINKS</span></span>

[<span data-ttu-id="81370-185">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="81370-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="81370-186">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="81370-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="81370-187">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="81370-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="81370-188">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="81370-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="81370-189">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="81370-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


