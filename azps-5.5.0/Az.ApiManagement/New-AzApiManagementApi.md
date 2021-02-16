---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 3312c725d63bcb42aab7d82144c5a8f6f8e67641
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235380"
---
# <span data-ttu-id="752f4-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="752f4-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="752f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="752f4-102">SYNOPSIS</span></span>
<span data-ttu-id="752f4-103">Создает API.</span><span class="sxs-lookup"><span data-stu-id="752f4-103">Creates an API.</span></span>

## <span data-ttu-id="752f4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="752f4-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="752f4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="752f4-105">DESCRIPTION</span></span>
<span data-ttu-id="752f4-106">Для создания API управления API Azure создается **cmdlet New-AzApiManagementApi.**</span><span class="sxs-lookup"><span data-stu-id="752f4-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="752f4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="752f4-107">EXAMPLES</span></span>

### <span data-ttu-id="752f4-108">Пример 1. Создание API</span><span class="sxs-lookup"><span data-stu-id="752f4-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="752f4-109">Эта команда создает API с именем EchoApi с указанным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="752f4-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="752f4-110">Пример 2. Создание API путем копирования всех операций, тегов, продуктов и политик из echo-api и в ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="752f4-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
```powershell
PS D:\github\azure-powershell>$context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso
PS D:\github\azure-powershell>$versionSet = Get-AzApiManagementApiVersionSet -Context $context -ApiVersionSetId "xmsVersionSet"
PS D:\github\azure-powershell> New-AzApiManagementApi -Context $context -Name "echoapiv4" -Description "Create Echo Api V4" -SubscriptionRequired -ServiceUrl "https://echoapi.cloudapp.net/v4" -Path "echov3" -Protocols @("http", "https") -ApiVersionSetId $versionSet.ApiVersionSetId -SourceApiId "echo-api" -ApiVersion "v4"


ApiId                         : 691b7d410125414a929c108541c60e06
Name                          : echoapiv4
Description                   : Create Echo Api V4
ServiceUrl                    : https://echoapi.cloudapp.net/v4 
Path                          : echov3
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v4
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/xmsVersionSet
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/691b7d410125414a929c108541c60e06    
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="752f4-111">Эта команда создает API в ApiVersionSet и копирует все операции, теги и политики `echoapiv3` `xmsVersionSet` из source `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="752f4-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="752f4-112">Она переопределяет протоколы SubscriptionRequired, ServiceUrl, Path и Protocols.</span><span class="sxs-lookup"><span data-stu-id="752f4-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="752f4-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="752f4-113">Example 3</span></span>

<span data-ttu-id="752f4-114">Создает API.</span><span class="sxs-lookup"><span data-stu-id="752f4-114">Creates an API.</span></span> <span data-ttu-id="752f4-115">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="752f4-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="752f4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="752f4-116">PARAMETERS</span></span>

### <span data-ttu-id="752f4-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="752f4-117">-ApiId</span></span>
<span data-ttu-id="752f4-118">Определяет ИД созда создаемого API.</span><span class="sxs-lookup"><span data-stu-id="752f4-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="752f4-119">Если этот параметр не задан, этот cmdlet создает для вас код.</span><span class="sxs-lookup"><span data-stu-id="752f4-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="752f4-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="752f4-120">-ApiVersion</span></span>
<span data-ttu-id="752f4-121">Создайте API-версию API.</span><span class="sxs-lookup"><span data-stu-id="752f4-121">Api Version of the Api to create.</span></span> <span data-ttu-id="752f4-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="752f4-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="752f4-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="752f4-123">-ApiVersionDescription</span></span>
<span data-ttu-id="752f4-124">Описание версии API.</span><span class="sxs-lookup"><span data-stu-id="752f4-124">Api Version Description.</span></span> <span data-ttu-id="752f4-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="752f4-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="752f4-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="752f4-126">-ApiVersionSetId</span></span>
<span data-ttu-id="752f4-127">Идентификатор ресурса для связанного набора версий API.</span><span class="sxs-lookup"><span data-stu-id="752f4-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="752f4-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="752f4-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="752f4-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="752f4-129">-AuthorizationScope</span></span>
<span data-ttu-id="752f4-130">Определяет область операций OAuth.</span><span class="sxs-lookup"><span data-stu-id="752f4-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="752f4-131">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="752f4-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="752f4-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="752f4-132">-AuthorizationServerId</span></span>
<span data-ttu-id="752f4-133">Определяет ИД сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="752f4-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="752f4-134">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="752f4-134">The default value is $Null.</span></span>
<span data-ttu-id="752f4-135">Этот параметр необходимо указать, *если задан параметр AuthorizationScope.*</span><span class="sxs-lookup"><span data-stu-id="752f4-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="752f4-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="752f4-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="752f4-137">Механизм сервера авторизации OpenId, с помощью которого маркер доступа передается в API.</span><span class="sxs-lookup"><span data-stu-id="752f4-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="752f4-138">Обратитесь к http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="752f4-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="752f4-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="752f4-139">This parameter is optional.</span></span> <span data-ttu-id="752f4-140">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="752f4-140">Default value is $null.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="752f4-141">-Контекст</span><span class="sxs-lookup"><span data-stu-id="752f4-141">-Context</span></span>
<span data-ttu-id="752f4-142">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="752f4-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="752f4-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="752f4-143">-DefaultProfile</span></span>
<span data-ttu-id="752f4-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="752f4-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="752f4-145">-Description</span><span class="sxs-lookup"><span data-stu-id="752f4-145">-Description</span></span>
<span data-ttu-id="752f4-146">Описание веб-API.</span><span class="sxs-lookup"><span data-stu-id="752f4-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="752f4-147">-Name</span><span class="sxs-lookup"><span data-stu-id="752f4-147">-Name</span></span>
<span data-ttu-id="752f4-148">Указывает имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="752f4-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="752f4-149">Это имя открытого API, которое отображается на порталах разработчика и администратора.</span><span class="sxs-lookup"><span data-stu-id="752f4-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="752f4-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="752f4-150">-OpenIdProviderId</span></span>
<span data-ttu-id="752f4-151">Идентификатор сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="752f4-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="752f4-152">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="752f4-152">This parameter is optional.</span></span> <span data-ttu-id="752f4-153">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="752f4-153">Default value is $null.</span></span> <span data-ttu-id="752f4-154">Должен быть указан, если указан BearerTokenSendingMethods.</span><span class="sxs-lookup"><span data-stu-id="752f4-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="752f4-155">-Path</span><span class="sxs-lookup"><span data-stu-id="752f4-155">-Path</span></span>
<span data-ttu-id="752f4-156">Путь к веб-интерфейсу API, который является последней частью url-адреса API и соответствует полю суффикса URL-адреса Web API на портале администрирования.</span><span class="sxs-lookup"><span data-stu-id="752f4-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="752f4-157">Этот URL-адрес используется пользователями API для отправки запросов веб-службе и должен иметь длину от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="752f4-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="752f4-158">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="752f4-158">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="752f4-159">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="752f4-159">-ProductIds</span></span>
<span data-ttu-id="752f4-160">Определяет массив ИД продуктов, в который нужно добавить новый API.</span><span class="sxs-lookup"><span data-stu-id="752f4-160">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="752f4-161">-Protocols</span><span class="sxs-lookup"><span data-stu-id="752f4-161">-Protocols</span></span>
<span data-ttu-id="752f4-162">Определяет массив протоколов веб-API.</span><span class="sxs-lookup"><span data-stu-id="752f4-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="752f4-163">Допустимые значения: http, https.</span><span class="sxs-lookup"><span data-stu-id="752f4-163">Valid values are http, https.</span></span>
<span data-ttu-id="752f4-164">Это веб-протоколы, на которых будет доступен API.</span><span class="sxs-lookup"><span data-stu-id="752f4-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="752f4-165">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="752f4-165">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="752f4-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="752f4-166">-ServiceUrl</span></span>
<span data-ttu-id="752f4-167">Url-адрес веб-службы, которая предоставляет API.</span><span class="sxs-lookup"><span data-stu-id="752f4-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="752f4-168">Этот URL-адрес используется только службой управления Azure API и не является общедоступным.</span><span class="sxs-lookup"><span data-stu-id="752f4-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="752f4-169">URL-адрес должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="752f4-169">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="752f4-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="752f4-170">-SourceApiId</span></span>
<span data-ttu-id="752f4-171">Идентификатор API источника API.</span><span class="sxs-lookup"><span data-stu-id="752f4-171">Api identifier of the source API.</span></span> <span data-ttu-id="752f4-172">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="752f4-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="752f4-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="752f4-173">-SourceApiRevision</span></span>
<span data-ttu-id="752f4-174">API Редакция для API источника.</span><span class="sxs-lookup"><span data-stu-id="752f4-174">Api Revision of the source API.</span></span> <span data-ttu-id="752f4-175">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="752f4-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="752f4-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="752f4-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="752f4-177">Указывает имя заглавного названия ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="752f4-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="752f4-178">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="752f4-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="752f4-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="752f4-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="752f4-180">Указывает имя параметра строки запроса к ключу подписки.</span><span class="sxs-lookup"><span data-stu-id="752f4-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="752f4-181">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="752f4-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="752f4-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="752f4-182">-SubscriptionRequired</span></span>
<span data-ttu-id="752f4-183">Флаг для принудительного использования SubscriptionRequired для запросов к Api.</span><span class="sxs-lookup"><span data-stu-id="752f4-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="752f4-184">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="752f4-184">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="752f4-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="752f4-185">CommonParameters</span></span>
<span data-ttu-id="752f4-186">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="752f4-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="752f4-187">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="752f4-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="752f4-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="752f4-188">INPUTS</span></span>

### <span data-ttu-id="752f4-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="752f4-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="752f4-190">System.String</span><span class="sxs-lookup"><span data-stu-id="752f4-190">System.String</span></span>

### <span data-ttu-id="752f4-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="752f4-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="752f4-192">System.String[]</span><span class="sxs-lookup"><span data-stu-id="752f4-192">System.String[]</span></span>

## <span data-ttu-id="752f4-193">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="752f4-193">OUTPUTS</span></span>

### <span data-ttu-id="752f4-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="752f4-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="752f4-195">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="752f4-195">NOTES</span></span>

## <span data-ttu-id="752f4-196">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="752f4-196">RELATED LINKS</span></span>

[<span data-ttu-id="752f4-197">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="752f4-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="752f4-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="752f4-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="752f4-199">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="752f4-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="752f4-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="752f4-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="752f4-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="752f4-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


