---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244381"
---
# <span data-ttu-id="6f985-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6f985-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="6f985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f985-102">SYNOPSIS</span></span>
<span data-ttu-id="6f985-103">Изменение редакции API</span><span class="sxs-lookup"><span data-stu-id="6f985-103">Modifies an API Revision</span></span>

## <span data-ttu-id="6f985-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6f985-104">SYNTAX</span></span>

### <span data-ttu-id="6f985-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f985-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f985-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6f985-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f985-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f985-107">DESCRIPTION</span></span>
<span data-ttu-id="6f985-108">**Cmdlet Set-AzApiManagementApiRevision** изменяет версию API управления Azure API.</span><span class="sxs-lookup"><span data-stu-id="6f985-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="6f985-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6f985-109">EXAMPLES</span></span>

### <span data-ttu-id="6f985-110">Пример 1. Изменение редакции API</span><span class="sxs-lookup"><span data-stu-id="6f985-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="6f985-111">Новый описание, протокол и путь к API обновляются `2` `echo-api` с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f985-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="6f985-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f985-112">PARAMETERS</span></span>

### <span data-ttu-id="6f985-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6f985-113">-ApiId</span></span>
<span data-ttu-id="6f985-114">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="6f985-114">Identifier of existing API.</span></span>
<span data-ttu-id="6f985-115">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="6f985-115">This parameter is required.</span></span>

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

### <span data-ttu-id="6f985-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6f985-116">-ApiRevision</span></span>
<span data-ttu-id="6f985-117">Идентификатор существующего изменения API.</span><span class="sxs-lookup"><span data-stu-id="6f985-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="6f985-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="6f985-118">This parameter is required.</span></span>

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

### <span data-ttu-id="6f985-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="6f985-119">-AuthorizationScope</span></span>
<span data-ttu-id="6f985-120">Область операций OAuth.</span><span class="sxs-lookup"><span data-stu-id="6f985-120">OAuth operations scope.</span></span>
<span data-ttu-id="6f985-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6f985-121">This parameter is optional.</span></span>
<span data-ttu-id="6f985-122">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="6f985-122">Default value is $null.</span></span>

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

### <span data-ttu-id="6f985-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="6f985-123">-AuthorizationServerId</span></span>
<span data-ttu-id="6f985-124">Идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="6f985-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="6f985-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6f985-125">This parameter is optional.</span></span>
<span data-ttu-id="6f985-126">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="6f985-126">Default value is $null.</span></span>
<span data-ttu-id="6f985-127">Требуется указать, если задана authorizationScope.</span><span class="sxs-lookup"><span data-stu-id="6f985-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="6f985-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="6f985-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="6f985-129">Механизм сервера авторизации OpenId, с помощью которого маркер доступа передается в API.</span><span class="sxs-lookup"><span data-stu-id="6f985-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="6f985-130">Обратитесь к http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="6f985-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="6f985-131">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6f985-131">This parameter is optional.</span></span> <span data-ttu-id="6f985-132">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="6f985-132">Default value is $null.</span></span>

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

### <span data-ttu-id="6f985-133">-Контекст</span><span class="sxs-lookup"><span data-stu-id="6f985-133">-Context</span></span>
<span data-ttu-id="6f985-134">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6f985-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6f985-135">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="6f985-135">This parameter is required.</span></span>

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

### <span data-ttu-id="6f985-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f985-136">-DefaultProfile</span></span>
<span data-ttu-id="6f985-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f985-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f985-138">-Description</span><span class="sxs-lookup"><span data-stu-id="6f985-138">-Description</span></span>
<span data-ttu-id="6f985-139">Описание Веб-API.</span><span class="sxs-lookup"><span data-stu-id="6f985-139">Web API description.</span></span>
<span data-ttu-id="6f985-140">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6f985-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f985-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f985-141">-InputObject</span></span>
<span data-ttu-id="6f985-142">Экземпляр PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="6f985-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="6f985-143">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="6f985-143">This parameter is required.</span></span>

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

### <span data-ttu-id="6f985-144">-Name</span><span class="sxs-lookup"><span data-stu-id="6f985-144">-Name</span></span>
<span data-ttu-id="6f985-145">Имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="6f985-145">Web API name.</span></span>
<span data-ttu-id="6f985-146">Имя API, которое будет отображаться на порталах разработчика и администратора.</span><span class="sxs-lookup"><span data-stu-id="6f985-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="6f985-147">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="6f985-147">This parameter is required.</span></span>

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

### <span data-ttu-id="6f985-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="6f985-148">-OpenIdProviderId</span></span>
<span data-ttu-id="6f985-149">Идентификатор сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="6f985-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="6f985-150">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6f985-150">This parameter is optional.</span></span> <span data-ttu-id="6f985-151">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="6f985-151">Default value is $null.</span></span> <span data-ttu-id="6f985-152">Должен быть указан, если указан BearerTokenSendingMethods.</span><span class="sxs-lookup"><span data-stu-id="6f985-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="6f985-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f985-153">-PassThru</span></span>
<span data-ttu-id="6f985-154">Если задан этот экземпляр, экземпляр Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi, представляющий собой API набора.</span><span class="sxs-lookup"><span data-stu-id="6f985-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="6f985-155">-Path</span><span class="sxs-lookup"><span data-stu-id="6f985-155">-Path</span></span>
<span data-ttu-id="6f985-156">Путь к Веб-API.</span><span class="sxs-lookup"><span data-stu-id="6f985-156">Web API Path.</span></span>
<span data-ttu-id="6f985-157">Последняя часть URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="6f985-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="6f985-158">Этот URL-адрес будет использоваться пользователями API для отправки запросов в веб-службу.</span><span class="sxs-lookup"><span data-stu-id="6f985-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="6f985-159">Должен иметь длину от 1 до 400 знаков.</span><span class="sxs-lookup"><span data-stu-id="6f985-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="6f985-160">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6f985-160">This parameter is optional.</span></span>
<span data-ttu-id="6f985-161">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="6f985-161">Default value is $null.</span></span>

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

### <span data-ttu-id="6f985-162">-Protocols</span><span class="sxs-lookup"><span data-stu-id="6f985-162">-Protocols</span></span>
<span data-ttu-id="6f985-163">Протоколы Web API (http, https).</span><span class="sxs-lookup"><span data-stu-id="6f985-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="6f985-164">Протоколы, для которых доступен API.</span><span class="sxs-lookup"><span data-stu-id="6f985-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="6f985-165">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="6f985-165">This parameter is required.</span></span>
<span data-ttu-id="6f985-166">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="6f985-166">Default value is $null.</span></span>

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

### <span data-ttu-id="6f985-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="6f985-167">-ServiceUrl</span></span>
<span data-ttu-id="6f985-168">URL-адрес веб-службы, предлагая API.</span><span class="sxs-lookup"><span data-stu-id="6f985-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="6f985-169">Этот URL-адрес будет использоваться только службой управления API Azure и не будет разоснана.</span><span class="sxs-lookup"><span data-stu-id="6f985-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="6f985-170">Должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="6f985-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="6f985-171">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="6f985-171">This parameter is required.</span></span>

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

### <span data-ttu-id="6f985-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="6f985-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="6f985-173">Имя заглавного имени ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="6f985-173">Subscription key header name.</span></span>
<span data-ttu-id="6f985-174">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6f985-174">This parameter is optional.</span></span>
<span data-ttu-id="6f985-175">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="6f985-175">Default value is $null.</span></span>

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

### <span data-ttu-id="6f985-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="6f985-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="6f985-177">Имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="6f985-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="6f985-178">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6f985-178">This parameter is optional.</span></span>
<span data-ttu-id="6f985-179">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="6f985-179">Default value is $null.</span></span>

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

### <span data-ttu-id="6f985-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="6f985-180">-SubscriptionRequired</span></span>
<span data-ttu-id="6f985-181">Флаг для принудительного использования SubscriptionRequired для запросов к Api.</span><span class="sxs-lookup"><span data-stu-id="6f985-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="6f985-182">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6f985-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="6f985-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f985-183">-Confirm</span></span>
<span data-ttu-id="6f985-184">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f985-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f985-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f985-185">-WhatIf</span></span>
<span data-ttu-id="6f985-186">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f985-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f985-187">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6f985-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f985-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f985-188">CommonParameters</span></span>
<span data-ttu-id="6f985-189">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f985-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f985-190">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f985-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f985-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f985-191">INPUTS</span></span>

### <span data-ttu-id="6f985-192">System.String</span><span class="sxs-lookup"><span data-stu-id="6f985-192">System.String</span></span>

### <span data-ttu-id="6f985-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6f985-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6f985-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f985-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="6f985-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="6f985-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="6f985-196">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6f985-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6f985-197">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6f985-197">OUTPUTS</span></span>

### <span data-ttu-id="6f985-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f985-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="6f985-199">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6f985-199">NOTES</span></span>

## <span data-ttu-id="6f985-200">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f985-200">RELATED LINKS</span></span>

[<span data-ttu-id="6f985-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6f985-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="6f985-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6f985-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="6f985-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6f985-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)