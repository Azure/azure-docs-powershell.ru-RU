---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: 8b2e29da3c3f6140cbab422e74d09656c921c16c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901598"
---
# <span data-ttu-id="1949d-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="1949d-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="1949d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1949d-102">SYNOPSIS</span></span>
<span data-ttu-id="1949d-103">Изменение редакции API</span><span class="sxs-lookup"><span data-stu-id="1949d-103">Modifies an API Revision</span></span>

## <span data-ttu-id="1949d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1949d-104">SYNTAX</span></span>

### <span data-ttu-id="1949d-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1949d-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1949d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1949d-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1949d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1949d-107">DESCRIPTION</span></span>
<span data-ttu-id="1949d-108">Командлет **Set-AzApiManagementApiRevision** изменяет версию API управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="1949d-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="1949d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1949d-109">EXAMPLES</span></span>

### <span data-ttu-id="1949d-110">Пример 1. изменение редакции API</span><span class="sxs-lookup"><span data-stu-id="1949d-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="1949d-111">Командлет обновляет `2` новую версию API `echo-api` с новым описанием, протоколом и путем.</span><span class="sxs-lookup"><span data-stu-id="1949d-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="1949d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1949d-112">PARAMETERS</span></span>

### <span data-ttu-id="1949d-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1949d-113">-ApiId</span></span>
<span data-ttu-id="1949d-114">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="1949d-114">Identifier of existing API.</span></span>
<span data-ttu-id="1949d-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1949d-115">This parameter is required.</span></span>

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

### <span data-ttu-id="1949d-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="1949d-116">-ApiRevision</span></span>
<span data-ttu-id="1949d-117">Идентификатор существующей редакции API.</span><span class="sxs-lookup"><span data-stu-id="1949d-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="1949d-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1949d-118">This parameter is required.</span></span>

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

### <span data-ttu-id="1949d-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="1949d-119">-AuthorizationScope</span></span>
<span data-ttu-id="1949d-120">Область действия для OAuth.</span><span class="sxs-lookup"><span data-stu-id="1949d-120">OAuth operations scope.</span></span>
<span data-ttu-id="1949d-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1949d-121">This parameter is optional.</span></span>
<span data-ttu-id="1949d-122">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="1949d-122">Default value is $null.</span></span>

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

### <span data-ttu-id="1949d-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="1949d-123">-AuthorizationServerId</span></span>
<span data-ttu-id="1949d-124">Идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="1949d-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="1949d-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1949d-125">This parameter is optional.</span></span>
<span data-ttu-id="1949d-126">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="1949d-126">Default value is $null.</span></span>
<span data-ttu-id="1949d-127">Должен быть указан, если указан AuthorizationScope.</span><span class="sxs-lookup"><span data-stu-id="1949d-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="1949d-128">-Context</span><span class="sxs-lookup"><span data-stu-id="1949d-128">-Context</span></span>
<span data-ttu-id="1949d-129">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1949d-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1949d-130">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1949d-130">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1949d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1949d-131">-DefaultProfile</span></span>
<span data-ttu-id="1949d-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1949d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1949d-133">-Описание</span><span class="sxs-lookup"><span data-stu-id="1949d-133">-Description</span></span>
<span data-ttu-id="1949d-134">Описание веб-API.</span><span class="sxs-lookup"><span data-stu-id="1949d-134">Web API description.</span></span>
<span data-ttu-id="1949d-135">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1949d-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="1949d-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1949d-136">-InputObject</span></span>
<span data-ttu-id="1949d-137">Экземпляр PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="1949d-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="1949d-138">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1949d-138">This parameter is required.</span></span>

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

### <span data-ttu-id="1949d-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1949d-139">-Name</span></span>
<span data-ttu-id="1949d-140">Имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="1949d-140">Web API name.</span></span>
<span data-ttu-id="1949d-141">Общедоступное имя API, которое будет отображаться на порталах разработчиков и администраторов.</span><span class="sxs-lookup"><span data-stu-id="1949d-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="1949d-142">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1949d-142">This parameter is required.</span></span>

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

### <span data-ttu-id="1949d-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1949d-143">-PassThru</span></span>
<span data-ttu-id="1949d-144">Если указан, то экземпляр типа Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi, представляющий API набора.</span><span class="sxs-lookup"><span data-stu-id="1949d-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="1949d-145">-Path</span><span class="sxs-lookup"><span data-stu-id="1949d-145">-Path</span></span>
<span data-ttu-id="1949d-146">Путь к веб-API.</span><span class="sxs-lookup"><span data-stu-id="1949d-146">Web API Path.</span></span>
<span data-ttu-id="1949d-147">Последняя часть общедоступного URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="1949d-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="1949d-148">Этот URL-адрес будет использоваться клиентами API для отправки запросов веб-службе.</span><span class="sxs-lookup"><span data-stu-id="1949d-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="1949d-149">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="1949d-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="1949d-150">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1949d-150">This parameter is optional.</span></span>
<span data-ttu-id="1949d-151">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="1949d-151">Default value is $null.</span></span>

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

### <span data-ttu-id="1949d-152">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="1949d-152">-Protocols</span></span>
<span data-ttu-id="1949d-153">Протоколы веб-API (HTTP, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="1949d-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="1949d-154">Протоколы, через которые API станет доступным.</span><span class="sxs-lookup"><span data-stu-id="1949d-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="1949d-155">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1949d-155">This parameter is required.</span></span>
<span data-ttu-id="1949d-156">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="1949d-156">Default value is $null.</span></span>

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

### <span data-ttu-id="1949d-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="1949d-157">-ServiceUrl</span></span>
<span data-ttu-id="1949d-158">URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="1949d-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="1949d-159">Этот URL-адрес будет использоваться только для управления API Azure и не будет открыт.</span><span class="sxs-lookup"><span data-stu-id="1949d-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="1949d-160">Должно содержать от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="1949d-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="1949d-161">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="1949d-161">This parameter is required.</span></span>

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

### <span data-ttu-id="1949d-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="1949d-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="1949d-163">Имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="1949d-163">Subscription key header name.</span></span>
<span data-ttu-id="1949d-164">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1949d-164">This parameter is optional.</span></span>
<span data-ttu-id="1949d-165">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="1949d-165">Default value is $null.</span></span>

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

### <span data-ttu-id="1949d-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="1949d-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="1949d-167">Имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="1949d-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="1949d-168">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1949d-168">This parameter is optional.</span></span>
<span data-ttu-id="1949d-169">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="1949d-169">Default value is $null.</span></span>

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

### <span data-ttu-id="1949d-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1949d-170">-Confirm</span></span>
<span data-ttu-id="1949d-171">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1949d-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1949d-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1949d-172">-WhatIf</span></span>
<span data-ttu-id="1949d-173">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1949d-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1949d-174">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1949d-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1949d-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1949d-175">CommonParameters</span></span>
<span data-ttu-id="1949d-176">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1949d-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1949d-177">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1949d-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1949d-178">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1949d-178">INPUTS</span></span>

### <span data-ttu-id="1949d-179">System. String</span><span class="sxs-lookup"><span data-stu-id="1949d-179">System.String</span></span>

### <span data-ttu-id="1949d-180">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1949d-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1949d-181">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1949d-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="1949d-182">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="1949d-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="1949d-183">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1949d-183">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1949d-184">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1949d-184">OUTPUTS</span></span>

### <span data-ttu-id="1949d-185">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1949d-185">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="1949d-186">Пуск</span><span class="sxs-lookup"><span data-stu-id="1949d-186">NOTES</span></span>

## <span data-ttu-id="1949d-187">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1949d-187">RELATED LINKS</span></span>

[<span data-ttu-id="1949d-188">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="1949d-188">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="1949d-189">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="1949d-189">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="1949d-190">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="1949d-190">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)