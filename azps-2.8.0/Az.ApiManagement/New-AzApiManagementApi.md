---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: b332ccc8dc9188259c897c53256f1a14fd96280e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728077"
---
# <span data-ttu-id="1236d-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1236d-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="1236d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1236d-102">SYNOPSIS</span></span>
<span data-ttu-id="1236d-103">Создание API.</span><span class="sxs-lookup"><span data-stu-id="1236d-103">Creates an API.</span></span>

## <span data-ttu-id="1236d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1236d-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1236d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1236d-105">DESCRIPTION</span></span>
<span data-ttu-id="1236d-106">Командлет **New-AzApiManagementApi** создает API управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="1236d-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="1236d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1236d-107">EXAMPLES</span></span>

### <span data-ttu-id="1236d-108">Пример 1: создание API</span><span class="sxs-lookup"><span data-stu-id="1236d-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="1236d-109">Эта команда создает API с именем EchoApi и указанным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="1236d-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="1236d-110">Пример 1: создание API путем копирования всех операций, тегов, продуктов и политик из Echo API и в ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1236d-110">Example 1: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="1236d-111">Эта команда создает API `echoapiv3` в ApiVersionSet `xmsVersionSet` и копирует все операции, теги и политики из исходного API `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="1236d-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="1236d-112">Переопределение SubscriptionRequired, ServiceUrl, Path, Protocols</span><span class="sxs-lookup"><span data-stu-id="1236d-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

## <span data-ttu-id="1236d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1236d-113">PARAMETERS</span></span>

### <span data-ttu-id="1236d-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1236d-114">-ApiId</span></span>
<span data-ttu-id="1236d-115">Указывает идентификатор создаваемого API.</span><span class="sxs-lookup"><span data-stu-id="1236d-115">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="1236d-116">Если этот параметр не указан, этот командлет создаст идентификатор.</span><span class="sxs-lookup"><span data-stu-id="1236d-116">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="1236d-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1236d-117">-ApiVersion</span></span>
<span data-ttu-id="1236d-118">Версия API создаваемого API-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1236d-118">Api Version of the Api to create.</span></span> <span data-ttu-id="1236d-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1236d-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="1236d-120">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="1236d-120">-ApiVersionDescription</span></span>
<span data-ttu-id="1236d-121">Описание версии API.</span><span class="sxs-lookup"><span data-stu-id="1236d-121">Api Version Description.</span></span> <span data-ttu-id="1236d-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1236d-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="1236d-123">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="1236d-123">-ApiVersionSetId</span></span>
<span data-ttu-id="1236d-124">Идентификатор ресурса для связанного набор версий API.</span><span class="sxs-lookup"><span data-stu-id="1236d-124">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="1236d-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1236d-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="1236d-126">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="1236d-126">-AuthorizationScope</span></span>
<span data-ttu-id="1236d-127">Указывает область действий OAuth.</span><span class="sxs-lookup"><span data-stu-id="1236d-127">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="1236d-128">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="1236d-128">The default value is $Null.</span></span>

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

### <span data-ttu-id="1236d-129">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="1236d-129">-AuthorizationServerId</span></span>
<span data-ttu-id="1236d-130">Указывает идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="1236d-130">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="1236d-131">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="1236d-131">The default value is $Null.</span></span>
<span data-ttu-id="1236d-132">Если указан *AuthorizationScope* , необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="1236d-132">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="1236d-133">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="1236d-133">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="1236d-134">Механизм сервера авторизации OpenId, с помощью которого токен доступа передается API-интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="1236d-134">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="1236d-135">Ссылка на http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="1236d-135">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="1236d-136">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1236d-136">This parameter is optional.</span></span> <span data-ttu-id="1236d-137">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="1236d-137">Default value is $null.</span></span>

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

### <span data-ttu-id="1236d-138">-Context</span><span class="sxs-lookup"><span data-stu-id="1236d-138">-Context</span></span>
<span data-ttu-id="1236d-139">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1236d-139">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1236d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1236d-140">-DefaultProfile</span></span>
<span data-ttu-id="1236d-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1236d-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1236d-142">-Описание</span><span class="sxs-lookup"><span data-stu-id="1236d-142">-Description</span></span>
<span data-ttu-id="1236d-143">Задает описание для веб-API.</span><span class="sxs-lookup"><span data-stu-id="1236d-143">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="1236d-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1236d-144">-Name</span></span>
<span data-ttu-id="1236d-145">Указывает имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="1236d-145">Specifies the name of the web API.</span></span>
<span data-ttu-id="1236d-146">Это общедоступное имя API, которое отображается на порталах разработчиков и администраторов.</span><span class="sxs-lookup"><span data-stu-id="1236d-146">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="1236d-147">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="1236d-147">-OpenIdProviderId</span></span>
<span data-ttu-id="1236d-148">Идентификатор сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="1236d-148">OpenId authorization server identifier.</span></span> <span data-ttu-id="1236d-149">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1236d-149">This parameter is optional.</span></span> <span data-ttu-id="1236d-150">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="1236d-150">Default value is $null.</span></span> <span data-ttu-id="1236d-151">Должен быть указан, если указан BearerTokenSendingMethods.</span><span class="sxs-lookup"><span data-stu-id="1236d-151">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="1236d-152">-Path</span><span class="sxs-lookup"><span data-stu-id="1236d-152">-Path</span></span>
<span data-ttu-id="1236d-153">Указывает путь веб-API, который является последней частью общедоступного URL-адреса API и соответствует полю суффикса URL-адреса Web API на портале администрирования.</span><span class="sxs-lookup"><span data-stu-id="1236d-153">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="1236d-154">Этот URL-адрес используется клиентами API для отправки запросов веб-службе и должен содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="1236d-154">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="1236d-155">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="1236d-155">The default value is $Null.</span></span>

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

### <span data-ttu-id="1236d-156">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1236d-156">-ProductIds</span></span>
<span data-ttu-id="1236d-157">Указывает массив идентификаторов продуктов, к которому нужно добавить новый API.</span><span class="sxs-lookup"><span data-stu-id="1236d-157">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="1236d-158">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="1236d-158">-Protocols</span></span>
<span data-ttu-id="1236d-159">Указывает массив протоколов веб-API.</span><span class="sxs-lookup"><span data-stu-id="1236d-159">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="1236d-160">Допустимые значения: HTTP, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1236d-160">Valid values are http, https.</span></span>
<span data-ttu-id="1236d-161">Это веб-протоколы, в которых интерфейс API становится доступным.</span><span class="sxs-lookup"><span data-stu-id="1236d-161">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="1236d-162">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="1236d-162">The default value is $Null.</span></span>

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

### <span data-ttu-id="1236d-163">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="1236d-163">-ServiceUrl</span></span>
<span data-ttu-id="1236d-164">Адрес URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="1236d-164">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="1236d-165">Этот URL-адрес используется только службой управления API Azure и не сделан общедоступным.</span><span class="sxs-lookup"><span data-stu-id="1236d-165">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="1236d-166">URL-адрес должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="1236d-166">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="1236d-167">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="1236d-167">-SourceApiId</span></span>
<span data-ttu-id="1236d-168">Идентификатор API исходного API.</span><span class="sxs-lookup"><span data-stu-id="1236d-168">Api identifier of the source API.</span></span> <span data-ttu-id="1236d-169">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1236d-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="1236d-170">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="1236d-170">-SourceApiRevision</span></span>
<span data-ttu-id="1236d-171">Версия API исходного API.</span><span class="sxs-lookup"><span data-stu-id="1236d-171">Api Revision of the source API.</span></span> <span data-ttu-id="1236d-172">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1236d-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="1236d-173">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="1236d-173">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="1236d-174">Задает имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="1236d-174">Specifies the subscription key header name.</span></span>
<span data-ttu-id="1236d-175">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="1236d-175">The default value is $Null.</span></span>

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

### <span data-ttu-id="1236d-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="1236d-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="1236d-177">Указывает имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="1236d-177">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="1236d-178">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="1236d-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="1236d-179">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="1236d-179">-SubscriptionRequired</span></span>
<span data-ttu-id="1236d-180">Пометка для принудительного применения SubscriptionRequired для запросов к API.</span><span class="sxs-lookup"><span data-stu-id="1236d-180">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="1236d-181">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1236d-181">This parameter is optional.</span></span>

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

### <span data-ttu-id="1236d-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1236d-182">CommonParameters</span></span>
<span data-ttu-id="1236d-183">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1236d-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1236d-184">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1236d-184">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1236d-185">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1236d-185">INPUTS</span></span>

### <span data-ttu-id="1236d-186">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1236d-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1236d-187">System. String</span><span class="sxs-lookup"><span data-stu-id="1236d-187">System.String</span></span>

### <span data-ttu-id="1236d-188">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="1236d-188">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="1236d-189">System. String []</span><span class="sxs-lookup"><span data-stu-id="1236d-189">System.String[]</span></span>

## <span data-ttu-id="1236d-190">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1236d-190">OUTPUTS</span></span>

### <span data-ttu-id="1236d-191">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1236d-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="1236d-192">Пуск</span><span class="sxs-lookup"><span data-stu-id="1236d-192">NOTES</span></span>

## <span data-ttu-id="1236d-193">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1236d-193">RELATED LINKS</span></span>

[<span data-ttu-id="1236d-194">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1236d-194">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="1236d-195">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1236d-195">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="1236d-196">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1236d-196">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="1236d-197">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1236d-197">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="1236d-198">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1236d-198">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


