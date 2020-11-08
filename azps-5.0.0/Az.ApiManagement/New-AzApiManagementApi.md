---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 3312c725d63bcb42aab7d82144c5a8f6f8e67641
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246458"
---
# <span data-ttu-id="7577f-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7577f-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="7577f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7577f-102">SYNOPSIS</span></span>
<span data-ttu-id="7577f-103">Создание API.</span><span class="sxs-lookup"><span data-stu-id="7577f-103">Creates an API.</span></span>

## <span data-ttu-id="7577f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7577f-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7577f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7577f-105">DESCRIPTION</span></span>
<span data-ttu-id="7577f-106">Командлет **New-AzApiManagementApi** создает API управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="7577f-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="7577f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7577f-107">EXAMPLES</span></span>

### <span data-ttu-id="7577f-108">Пример 1: создание API</span><span class="sxs-lookup"><span data-stu-id="7577f-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="7577f-109">Эта команда создает API с именем EchoApi и указанным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="7577f-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="7577f-110">Пример 2: создание API-интерфейса путем копирования всех операций, тегов, продуктов и политик из Echo-API и в ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="7577f-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="7577f-111">Эта команда создает API `echoapiv3` в ApiVersionSet `xmsVersionSet` и копирует все операции, теги и политики из исходного API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="7577f-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="7577f-112">Переопределение SubscriptionRequired, ServiceUrl, Path, Protocols</span><span class="sxs-lookup"><span data-stu-id="7577f-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="7577f-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7577f-113">Example 3</span></span>

<span data-ttu-id="7577f-114">Создание API.</span><span class="sxs-lookup"><span data-stu-id="7577f-114">Creates an API.</span></span> <span data-ttu-id="7577f-115">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="7577f-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="7577f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7577f-116">PARAMETERS</span></span>

### <span data-ttu-id="7577f-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7577f-117">-ApiId</span></span>
<span data-ttu-id="7577f-118">Указывает идентификатор создаваемого API.</span><span class="sxs-lookup"><span data-stu-id="7577f-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="7577f-119">Если этот параметр не указан, этот командлет создаст идентификатор.</span><span class="sxs-lookup"><span data-stu-id="7577f-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="7577f-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7577f-120">-ApiVersion</span></span>
<span data-ttu-id="7577f-121">Версия API создаваемого API-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7577f-121">Api Version of the Api to create.</span></span> <span data-ttu-id="7577f-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7577f-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="7577f-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="7577f-123">-ApiVersionDescription</span></span>
<span data-ttu-id="7577f-124">Описание версии API.</span><span class="sxs-lookup"><span data-stu-id="7577f-124">Api Version Description.</span></span> <span data-ttu-id="7577f-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7577f-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="7577f-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="7577f-126">-ApiVersionSetId</span></span>
<span data-ttu-id="7577f-127">Идентификатор ресурса для связанного набор версий API.</span><span class="sxs-lookup"><span data-stu-id="7577f-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="7577f-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7577f-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="7577f-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="7577f-129">-AuthorizationScope</span></span>
<span data-ttu-id="7577f-130">Указывает область действий OAuth.</span><span class="sxs-lookup"><span data-stu-id="7577f-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="7577f-131">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="7577f-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="7577f-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="7577f-132">-AuthorizationServerId</span></span>
<span data-ttu-id="7577f-133">Указывает идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="7577f-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="7577f-134">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="7577f-134">The default value is $Null.</span></span>
<span data-ttu-id="7577f-135">Если указан *AuthorizationScope* , необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7577f-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="7577f-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="7577f-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="7577f-137">Механизм сервера авторизации OpenId, с помощью которого токен доступа передается API-интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="7577f-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="7577f-138">Ссылка на http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="7577f-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="7577f-139">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7577f-139">This parameter is optional.</span></span> <span data-ttu-id="7577f-140">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="7577f-140">Default value is $null.</span></span>

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

### <span data-ttu-id="7577f-141">-Context</span><span class="sxs-lookup"><span data-stu-id="7577f-141">-Context</span></span>
<span data-ttu-id="7577f-142">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7577f-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7577f-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7577f-143">-DefaultProfile</span></span>
<span data-ttu-id="7577f-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7577f-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7577f-145">-Описание</span><span class="sxs-lookup"><span data-stu-id="7577f-145">-Description</span></span>
<span data-ttu-id="7577f-146">Задает описание для веб-API.</span><span class="sxs-lookup"><span data-stu-id="7577f-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="7577f-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7577f-147">-Name</span></span>
<span data-ttu-id="7577f-148">Указывает имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="7577f-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="7577f-149">Это общедоступное имя API, которое отображается на порталах разработчиков и администраторов.</span><span class="sxs-lookup"><span data-stu-id="7577f-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="7577f-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="7577f-150">-OpenIdProviderId</span></span>
<span data-ttu-id="7577f-151">Идентификатор сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="7577f-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="7577f-152">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7577f-152">This parameter is optional.</span></span> <span data-ttu-id="7577f-153">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="7577f-153">Default value is $null.</span></span> <span data-ttu-id="7577f-154">Должен быть указан, если указан BearerTokenSendingMethods.</span><span class="sxs-lookup"><span data-stu-id="7577f-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="7577f-155">-Path</span><span class="sxs-lookup"><span data-stu-id="7577f-155">-Path</span></span>
<span data-ttu-id="7577f-156">Указывает путь веб-API, который является последней частью общедоступного URL-адреса API и соответствует полю суффикса URL-адреса Web API на портале администрирования.</span><span class="sxs-lookup"><span data-stu-id="7577f-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="7577f-157">Этот URL-адрес используется клиентами API для отправки запросов веб-службе и должен содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="7577f-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="7577f-158">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="7577f-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="7577f-159">-ProductId</span><span class="sxs-lookup"><span data-stu-id="7577f-159">-ProductIds</span></span>
<span data-ttu-id="7577f-160">Указывает массив идентификаторов продуктов, к которому нужно добавить новый API.</span><span class="sxs-lookup"><span data-stu-id="7577f-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="7577f-161">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="7577f-161">-Protocols</span></span>
<span data-ttu-id="7577f-162">Указывает массив протоколов веб-API.</span><span class="sxs-lookup"><span data-stu-id="7577f-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="7577f-163">Допустимые значения: HTTP, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7577f-163">Valid values are http, https.</span></span>
<span data-ttu-id="7577f-164">Это веб-протоколы, в которых интерфейс API становится доступным.</span><span class="sxs-lookup"><span data-stu-id="7577f-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="7577f-165">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="7577f-165">The default value is $Null.</span></span>

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

### <span data-ttu-id="7577f-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="7577f-166">-ServiceUrl</span></span>
<span data-ttu-id="7577f-167">Адрес URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="7577f-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="7577f-168">Этот URL-адрес используется только службой управления API Azure и не сделан общедоступным.</span><span class="sxs-lookup"><span data-stu-id="7577f-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="7577f-169">URL-адрес должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="7577f-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="7577f-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="7577f-170">-SourceApiId</span></span>
<span data-ttu-id="7577f-171">Идентификатор API исходного API.</span><span class="sxs-lookup"><span data-stu-id="7577f-171">Api identifier of the source API.</span></span> <span data-ttu-id="7577f-172">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7577f-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="7577f-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="7577f-173">-SourceApiRevision</span></span>
<span data-ttu-id="7577f-174">Версия API исходного API.</span><span class="sxs-lookup"><span data-stu-id="7577f-174">Api Revision of the source API.</span></span> <span data-ttu-id="7577f-175">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7577f-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="7577f-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="7577f-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="7577f-177">Задает имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="7577f-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="7577f-178">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="7577f-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="7577f-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="7577f-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="7577f-180">Указывает имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="7577f-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="7577f-181">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="7577f-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="7577f-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="7577f-182">-SubscriptionRequired</span></span>
<span data-ttu-id="7577f-183">Пометка для принудительного применения SubscriptionRequired для запросов к API.</span><span class="sxs-lookup"><span data-stu-id="7577f-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="7577f-184">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="7577f-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="7577f-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7577f-185">CommonParameters</span></span>
<span data-ttu-id="7577f-186">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7577f-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7577f-187">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7577f-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7577f-188">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7577f-188">INPUTS</span></span>

### <span data-ttu-id="7577f-189">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7577f-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7577f-190">System. String</span><span class="sxs-lookup"><span data-stu-id="7577f-190">System.String</span></span>

### <span data-ttu-id="7577f-191">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="7577f-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="7577f-192">System. String []</span><span class="sxs-lookup"><span data-stu-id="7577f-192">System.String[]</span></span>

## <span data-ttu-id="7577f-193">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7577f-193">OUTPUTS</span></span>

### <span data-ttu-id="7577f-194">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7577f-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="7577f-195">Пуск</span><span class="sxs-lookup"><span data-stu-id="7577f-195">NOTES</span></span>

## <span data-ttu-id="7577f-196">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7577f-196">RELATED LINKS</span></span>

[<span data-ttu-id="7577f-197">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7577f-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="7577f-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7577f-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="7577f-199">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7577f-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="7577f-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7577f-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="7577f-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="7577f-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


