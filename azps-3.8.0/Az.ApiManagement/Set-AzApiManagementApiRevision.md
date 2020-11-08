---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: e7074b799e1c664ceb17499b04b8d4d2ff3acb5d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073864"
---
# <span data-ttu-id="42c16-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="42c16-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="42c16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42c16-102">SYNOPSIS</span></span>
<span data-ttu-id="42c16-103">Изменение редакции API</span><span class="sxs-lookup"><span data-stu-id="42c16-103">Modifies an API Revision</span></span>

## <span data-ttu-id="42c16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42c16-104">SYNTAX</span></span>

### <span data-ttu-id="42c16-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42c16-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42c16-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="42c16-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42c16-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42c16-107">DESCRIPTION</span></span>
<span data-ttu-id="42c16-108">Командлет **Set-AzApiManagementApiRevision** изменяет версию API управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="42c16-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="42c16-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42c16-109">EXAMPLES</span></span>

### <span data-ttu-id="42c16-110">Пример 1. изменение редакции API</span><span class="sxs-lookup"><span data-stu-id="42c16-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="42c16-111">Командлет обновляет `2` новую версию API `echo-api` с новым описанием, протоколом и путем.</span><span class="sxs-lookup"><span data-stu-id="42c16-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="42c16-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42c16-112">PARAMETERS</span></span>

### <span data-ttu-id="42c16-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="42c16-113">-ApiId</span></span>
<span data-ttu-id="42c16-114">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="42c16-114">Identifier of existing API.</span></span>
<span data-ttu-id="42c16-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42c16-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="42c16-116">-ApiRevision</span></span>
<span data-ttu-id="42c16-117">Идентификатор существующей редакции API.</span><span class="sxs-lookup"><span data-stu-id="42c16-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="42c16-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42c16-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="42c16-119">-AuthorizationScope</span></span>
<span data-ttu-id="42c16-120">Область действия для OAuth.</span><span class="sxs-lookup"><span data-stu-id="42c16-120">OAuth operations scope.</span></span>
<span data-ttu-id="42c16-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-121">This parameter is optional.</span></span>
<span data-ttu-id="42c16-122">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="42c16-122">Default value is $null.</span></span>

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

### <span data-ttu-id="42c16-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="42c16-123">-AuthorizationServerId</span></span>
<span data-ttu-id="42c16-124">Идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="42c16-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="42c16-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-125">This parameter is optional.</span></span>
<span data-ttu-id="42c16-126">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="42c16-126">Default value is $null.</span></span>
<span data-ttu-id="42c16-127">Должен быть указан, если указан AuthorizationScope.</span><span class="sxs-lookup"><span data-stu-id="42c16-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="42c16-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="42c16-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="42c16-129">Механизм сервера авторизации OpenId, с помощью которого токен доступа передается API-интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="42c16-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="42c16-130">Ссылка на http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="42c16-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="42c16-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-131">This parameter is optional.</span></span> <span data-ttu-id="42c16-132">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="42c16-132">Default value is $null.</span></span>

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

### <span data-ttu-id="42c16-133">-Context</span><span class="sxs-lookup"><span data-stu-id="42c16-133">-Context</span></span>
<span data-ttu-id="42c16-134">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="42c16-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="42c16-135">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-135">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42c16-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c16-136">-DefaultProfile</span></span>
<span data-ttu-id="42c16-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42c16-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42c16-138">-Описание</span><span class="sxs-lookup"><span data-stu-id="42c16-138">-Description</span></span>
<span data-ttu-id="42c16-139">Описание веб-API.</span><span class="sxs-lookup"><span data-stu-id="42c16-139">Web API description.</span></span>
<span data-ttu-id="42c16-140">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="42c16-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42c16-141">-InputObject</span></span>
<span data-ttu-id="42c16-142">Экземпляр PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="42c16-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="42c16-143">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-143">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42c16-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="42c16-144">-Name</span></span>
<span data-ttu-id="42c16-145">Имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="42c16-145">Web API name.</span></span>
<span data-ttu-id="42c16-146">Общедоступное имя API, которое будет отображаться на порталах разработчиков и администраторов.</span><span class="sxs-lookup"><span data-stu-id="42c16-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="42c16-147">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-147">This parameter is required.</span></span>

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

### <span data-ttu-id="42c16-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="42c16-148">-OpenIdProviderId</span></span>
<span data-ttu-id="42c16-149">Идентификатор сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="42c16-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="42c16-150">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-150">This parameter is optional.</span></span> <span data-ttu-id="42c16-151">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="42c16-151">Default value is $null.</span></span> <span data-ttu-id="42c16-152">Должен быть указан, если указан BearerTokenSendingMethods.</span><span class="sxs-lookup"><span data-stu-id="42c16-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="42c16-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="42c16-153">-PassThru</span></span>
<span data-ttu-id="42c16-154">Если указан, то экземпляр типа Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi, представляющий API набора.</span><span class="sxs-lookup"><span data-stu-id="42c16-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="42c16-155">-Path</span><span class="sxs-lookup"><span data-stu-id="42c16-155">-Path</span></span>
<span data-ttu-id="42c16-156">Путь к веб-API.</span><span class="sxs-lookup"><span data-stu-id="42c16-156">Web API Path.</span></span>
<span data-ttu-id="42c16-157">Последняя часть общедоступного URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="42c16-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="42c16-158">Этот URL-адрес будет использоваться клиентами API для отправки запросов веб-службе.</span><span class="sxs-lookup"><span data-stu-id="42c16-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="42c16-159">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="42c16-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="42c16-160">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-160">This parameter is optional.</span></span>
<span data-ttu-id="42c16-161">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="42c16-161">Default value is $null.</span></span>

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

### <span data-ttu-id="42c16-162">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="42c16-162">-Protocols</span></span>
<span data-ttu-id="42c16-163">Протоколы веб-API (HTTP, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="42c16-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="42c16-164">Протоколы, через которые API станет доступным.</span><span class="sxs-lookup"><span data-stu-id="42c16-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="42c16-165">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-165">This parameter is required.</span></span>
<span data-ttu-id="42c16-166">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="42c16-166">Default value is $null.</span></span>

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

### <span data-ttu-id="42c16-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="42c16-167">-ServiceUrl</span></span>
<span data-ttu-id="42c16-168">URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="42c16-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="42c16-169">Этот URL-адрес будет использоваться только для управления API Azure и не будет открыт.</span><span class="sxs-lookup"><span data-stu-id="42c16-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="42c16-170">Должно содержать от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="42c16-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="42c16-171">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-171">This parameter is required.</span></span>

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

### <span data-ttu-id="42c16-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="42c16-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="42c16-173">Имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="42c16-173">Subscription key header name.</span></span>
<span data-ttu-id="42c16-174">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-174">This parameter is optional.</span></span>
<span data-ttu-id="42c16-175">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="42c16-175">Default value is $null.</span></span>

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

### <span data-ttu-id="42c16-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="42c16-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="42c16-177">Имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="42c16-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="42c16-178">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-178">This parameter is optional.</span></span>
<span data-ttu-id="42c16-179">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="42c16-179">Default value is $null.</span></span>

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

### <span data-ttu-id="42c16-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="42c16-180">-SubscriptionRequired</span></span>
<span data-ttu-id="42c16-181">Пометка для принудительного применения SubscriptionRequired для запросов к API.</span><span class="sxs-lookup"><span data-stu-id="42c16-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="42c16-182">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="42c16-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="42c16-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42c16-183">-Confirm</span></span>
<span data-ttu-id="42c16-184">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42c16-184">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c16-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42c16-185">-WhatIf</span></span>
<span data-ttu-id="42c16-186">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42c16-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42c16-187">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42c16-187">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c16-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c16-188">CommonParameters</span></span>
<span data-ttu-id="42c16-189">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42c16-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c16-190">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42c16-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c16-191">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42c16-191">INPUTS</span></span>

### <span data-ttu-id="42c16-192">System. String</span><span class="sxs-lookup"><span data-stu-id="42c16-192">System.String</span></span>

### <span data-ttu-id="42c16-193">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="42c16-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="42c16-194">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="42c16-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="42c16-195">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="42c16-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="42c16-196">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="42c16-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="42c16-197">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42c16-197">OUTPUTS</span></span>

### <span data-ttu-id="42c16-198">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="42c16-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="42c16-199">Пуск</span><span class="sxs-lookup"><span data-stu-id="42c16-199">NOTES</span></span>

## <span data-ttu-id="42c16-200">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42c16-200">RELATED LINKS</span></span>

[<span data-ttu-id="42c16-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="42c16-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="42c16-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="42c16-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="42c16-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="42c16-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)