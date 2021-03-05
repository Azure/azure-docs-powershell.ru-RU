---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: b8eac81d90f20617399048464ecca40e0df8d93f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965512"
---
# <span data-ttu-id="984ee-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="984ee-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="984ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="984ee-102">SYNOPSIS</span></span>
<span data-ttu-id="984ee-103">Изменение редакции API</span><span class="sxs-lookup"><span data-stu-id="984ee-103">Modifies an API Revision</span></span>

## <span data-ttu-id="984ee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="984ee-104">SYNTAX</span></span>

### <span data-ttu-id="984ee-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="984ee-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="984ee-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="984ee-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="984ee-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="984ee-107">DESCRIPTION</span></span>
<span data-ttu-id="984ee-108">**Cmdlet Set-AzApiManagementApiRevision** изменяет версию API управления Azure API.</span><span class="sxs-lookup"><span data-stu-id="984ee-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="984ee-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="984ee-109">EXAMPLES</span></span>

### <span data-ttu-id="984ee-110">Пример 1. Изменение редакции API</span><span class="sxs-lookup"><span data-stu-id="984ee-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="984ee-111">Новый описание, протокол и путь к `2` API `echo-api` обновляется с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="984ee-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="984ee-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="984ee-112">PARAMETERS</span></span>

### <span data-ttu-id="984ee-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="984ee-113">-ApiId</span></span>
<span data-ttu-id="984ee-114">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="984ee-114">Identifier of existing API.</span></span>
<span data-ttu-id="984ee-115">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="984ee-115">This parameter is required.</span></span>

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

### <span data-ttu-id="984ee-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="984ee-116">-ApiRevision</span></span>
<span data-ttu-id="984ee-117">Идентификатор существующего изменения API.</span><span class="sxs-lookup"><span data-stu-id="984ee-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="984ee-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="984ee-118">This parameter is required.</span></span>

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

### <span data-ttu-id="984ee-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="984ee-119">-AuthorizationScope</span></span>
<span data-ttu-id="984ee-120">Область операций OAuth.</span><span class="sxs-lookup"><span data-stu-id="984ee-120">OAuth operations scope.</span></span>
<span data-ttu-id="984ee-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="984ee-121">This parameter is optional.</span></span>
<span data-ttu-id="984ee-122">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="984ee-122">Default value is $null.</span></span>

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

### <span data-ttu-id="984ee-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="984ee-123">-AuthorizationServerId</span></span>
<span data-ttu-id="984ee-124">Идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="984ee-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="984ee-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="984ee-125">This parameter is optional.</span></span>
<span data-ttu-id="984ee-126">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="984ee-126">Default value is $null.</span></span>
<span data-ttu-id="984ee-127">Требуется указать, если задана authorizationScope.</span><span class="sxs-lookup"><span data-stu-id="984ee-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="984ee-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="984ee-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="984ee-129">Механизм сервера авторизации OpenId, с помощью которого маркер доступа передается в API.</span><span class="sxs-lookup"><span data-stu-id="984ee-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="984ee-130">Обратитесь к http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="984ee-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="984ee-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="984ee-131">This parameter is optional.</span></span> <span data-ttu-id="984ee-132">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="984ee-132">Default value is $null.</span></span>

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

### <span data-ttu-id="984ee-133">-Контекст</span><span class="sxs-lookup"><span data-stu-id="984ee-133">-Context</span></span>
<span data-ttu-id="984ee-134">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="984ee-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="984ee-135">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="984ee-135">This parameter is required.</span></span>

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

### <span data-ttu-id="984ee-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="984ee-136">-DefaultProfile</span></span>
<span data-ttu-id="984ee-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="984ee-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="984ee-138">-Description</span><span class="sxs-lookup"><span data-stu-id="984ee-138">-Description</span></span>
<span data-ttu-id="984ee-139">Описание Веб-API.</span><span class="sxs-lookup"><span data-stu-id="984ee-139">Web API description.</span></span>
<span data-ttu-id="984ee-140">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="984ee-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="984ee-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="984ee-141">-InputObject</span></span>
<span data-ttu-id="984ee-142">Экземпляр PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="984ee-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="984ee-143">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="984ee-143">This parameter is required.</span></span>

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

### <span data-ttu-id="984ee-144">-Name</span><span class="sxs-lookup"><span data-stu-id="984ee-144">-Name</span></span>
<span data-ttu-id="984ee-145">Имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="984ee-145">Web API name.</span></span>
<span data-ttu-id="984ee-146">Имя API, которое будет отображаться на порталах разработчика и администратора.</span><span class="sxs-lookup"><span data-stu-id="984ee-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="984ee-147">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="984ee-147">This parameter is required.</span></span>

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

### <span data-ttu-id="984ee-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="984ee-148">-OpenIdProviderId</span></span>
<span data-ttu-id="984ee-149">Идентификатор сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="984ee-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="984ee-150">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="984ee-150">This parameter is optional.</span></span> <span data-ttu-id="984ee-151">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="984ee-151">Default value is $null.</span></span> <span data-ttu-id="984ee-152">Должен быть указан, если указан BearerTokenSendingMethods.</span><span class="sxs-lookup"><span data-stu-id="984ee-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="984ee-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="984ee-153">-PassThru</span></span>
<span data-ttu-id="984ee-154">Если задан этот экземпляр, экземпляр Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi, представляющий API набора.</span><span class="sxs-lookup"><span data-stu-id="984ee-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="984ee-155">-Path</span><span class="sxs-lookup"><span data-stu-id="984ee-155">-Path</span></span>
<span data-ttu-id="984ee-156">Путь к Веб-API.</span><span class="sxs-lookup"><span data-stu-id="984ee-156">Web API Path.</span></span>
<span data-ttu-id="984ee-157">Последняя часть URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="984ee-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="984ee-158">Этот URL-адрес будет использоваться пользователями API для отправки запросов в веб-службу.</span><span class="sxs-lookup"><span data-stu-id="984ee-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="984ee-159">Должен иметь длину от 1 до 400 знаков.</span><span class="sxs-lookup"><span data-stu-id="984ee-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="984ee-160">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="984ee-160">This parameter is optional.</span></span>
<span data-ttu-id="984ee-161">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="984ee-161">Default value is $null.</span></span>

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

### <span data-ttu-id="984ee-162">-Protocols</span><span class="sxs-lookup"><span data-stu-id="984ee-162">-Protocols</span></span>
<span data-ttu-id="984ee-163">Протоколы Web API (http, https).</span><span class="sxs-lookup"><span data-stu-id="984ee-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="984ee-164">Протоколы, для которых доступен API.</span><span class="sxs-lookup"><span data-stu-id="984ee-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="984ee-165">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="984ee-165">This parameter is required.</span></span>
<span data-ttu-id="984ee-166">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="984ee-166">Default value is $null.</span></span>

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

### <span data-ttu-id="984ee-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="984ee-167">-ServiceUrl</span></span>
<span data-ttu-id="984ee-168">URL-адрес веб-службы, предлагая API.</span><span class="sxs-lookup"><span data-stu-id="984ee-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="984ee-169">Этот URL-адрес будет использоваться только службой управления API Azure и не будет разоснана.</span><span class="sxs-lookup"><span data-stu-id="984ee-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="984ee-170">Должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="984ee-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="984ee-171">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="984ee-171">This parameter is required.</span></span>

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

### <span data-ttu-id="984ee-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="984ee-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="984ee-173">Имя заглавного имени ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="984ee-173">Subscription key header name.</span></span>
<span data-ttu-id="984ee-174">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="984ee-174">This parameter is optional.</span></span>
<span data-ttu-id="984ee-175">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="984ee-175">Default value is $null.</span></span>

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

### <span data-ttu-id="984ee-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="984ee-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="984ee-177">Имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="984ee-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="984ee-178">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="984ee-178">This parameter is optional.</span></span>
<span data-ttu-id="984ee-179">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="984ee-179">Default value is $null.</span></span>

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

### <span data-ttu-id="984ee-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="984ee-180">-SubscriptionRequired</span></span>
<span data-ttu-id="984ee-181">Флаг для принудительного использования SubscriptionRequired для запросов к Api.</span><span class="sxs-lookup"><span data-stu-id="984ee-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="984ee-182">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="984ee-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="984ee-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="984ee-183">-Confirm</span></span>
<span data-ttu-id="984ee-184">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="984ee-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="984ee-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="984ee-185">-WhatIf</span></span>
<span data-ttu-id="984ee-186">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="984ee-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="984ee-187">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="984ee-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="984ee-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="984ee-188">CommonParameters</span></span>
<span data-ttu-id="984ee-189">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="984ee-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="984ee-190">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="984ee-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="984ee-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="984ee-191">INPUTS</span></span>

### <span data-ttu-id="984ee-192">System.String</span><span class="sxs-lookup"><span data-stu-id="984ee-192">System.String</span></span>

### <span data-ttu-id="984ee-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="984ee-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="984ee-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="984ee-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="984ee-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="984ee-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="984ee-196">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="984ee-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="984ee-197">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="984ee-197">OUTPUTS</span></span>

### <span data-ttu-id="984ee-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="984ee-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="984ee-199">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="984ee-199">NOTES</span></span>

## <span data-ttu-id="984ee-200">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="984ee-200">RELATED LINKS</span></span>

[<span data-ttu-id="984ee-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="984ee-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="984ee-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="984ee-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="984ee-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="984ee-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)