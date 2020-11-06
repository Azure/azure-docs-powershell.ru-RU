---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: fe709b560c790ad010469bf2f0a2043231124138
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567318"
---
# <span data-ttu-id="9f7d6-101">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="9f7d6-101">Set-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="9f7d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f7d6-102">SYNOPSIS</span></span>
<span data-ttu-id="9f7d6-103">Изменение редакции API</span><span class="sxs-lookup"><span data-stu-id="9f7d6-103">Modifies an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f7d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f7d6-104">SYNTAX</span></span>

### <span data-ttu-id="9f7d6-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f7d6-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f7d6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9f7d6-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f7d6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f7d6-107">DESCRIPTION</span></span>
<span data-ttu-id="9f7d6-108">Командлет **Set-AzureRmApiManagementApiRevision** изменяет версию API управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-108">The **Set-AzureRmApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="9f7d6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f7d6-109">EXAMPLES</span></span>

### <span data-ttu-id="9f7d6-110">Пример 1. изменение редакции API</span><span class="sxs-lookup"><span data-stu-id="9f7d6-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="9f7d6-111">Командлет обновляет `2` новую версию API `echo-api` с новым описанием, протоколом и путем.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="9f7d6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f7d6-112">PARAMETERS</span></span>

### <span data-ttu-id="9f7d6-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9f7d6-113">-ApiId</span></span>
<span data-ttu-id="9f7d6-114">Идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-114">Identifier of existing API.</span></span>
<span data-ttu-id="9f7d6-115">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-115">This parameter is required.</span></span>

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

### <span data-ttu-id="9f7d6-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="9f7d6-116">-ApiRevision</span></span>
<span data-ttu-id="9f7d6-117">Идентификатор существующей редакции API.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="9f7d6-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-118">This parameter is required.</span></span>

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

### <span data-ttu-id="9f7d6-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="9f7d6-119">-AuthorizationScope</span></span>
<span data-ttu-id="9f7d6-120">Область действия для OAuth.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-120">OAuth operations scope.</span></span>
<span data-ttu-id="9f7d6-121">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-121">This parameter is optional.</span></span>
<span data-ttu-id="9f7d6-122">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-122">Default value is $null.</span></span>

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

### <span data-ttu-id="9f7d6-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="9f7d6-123">-AuthorizationServerId</span></span>
<span data-ttu-id="9f7d6-124">Идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="9f7d6-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-125">This parameter is optional.</span></span>
<span data-ttu-id="9f7d6-126">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-126">Default value is $null.</span></span>
<span data-ttu-id="9f7d6-127">Должен быть указан, если указан AuthorizationScope.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="9f7d6-128">-Context</span><span class="sxs-lookup"><span data-stu-id="9f7d6-128">-Context</span></span>
<span data-ttu-id="9f7d6-129">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9f7d6-130">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-130">This parameter is required.</span></span>

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

### <span data-ttu-id="9f7d6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f7d6-131">-DefaultProfile</span></span>
<span data-ttu-id="9f7d6-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f7d6-133">-Описание</span><span class="sxs-lookup"><span data-stu-id="9f7d6-133">-Description</span></span>
<span data-ttu-id="9f7d6-134">Описание веб-API.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-134">Web API description.</span></span>
<span data-ttu-id="9f7d6-135">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="9f7d6-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f7d6-136">-InputObject</span></span>
<span data-ttu-id="9f7d6-137">Экземпляр PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="9f7d6-138">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-138">This parameter is required.</span></span>

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

### <span data-ttu-id="9f7d6-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9f7d6-139">-Name</span></span>
<span data-ttu-id="9f7d6-140">Имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-140">Web API name.</span></span>
<span data-ttu-id="9f7d6-141">Общедоступное имя API, которое будет отображаться на порталах разработчиков и администраторов.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="9f7d6-142">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-142">This parameter is required.</span></span>

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

### <span data-ttu-id="9f7d6-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f7d6-143">-PassThru</span></span>
<span data-ttu-id="9f7d6-144">Если указан, то экземпляр типа Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi, представляющий API набора.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="9f7d6-145">-Path</span><span class="sxs-lookup"><span data-stu-id="9f7d6-145">-Path</span></span>
<span data-ttu-id="9f7d6-146">Путь к веб-API.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-146">Web API Path.</span></span>
<span data-ttu-id="9f7d6-147">Последняя часть общедоступного URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="9f7d6-148">Этот URL-адрес будет использоваться клиентами API для отправки запросов веб-службе.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="9f7d6-149">Должно содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="9f7d6-150">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-150">This parameter is optional.</span></span>
<span data-ttu-id="9f7d6-151">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-151">Default value is $null.</span></span>

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

### <span data-ttu-id="9f7d6-152">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="9f7d6-152">-Protocols</span></span>
<span data-ttu-id="9f7d6-153">Протоколы веб-API (HTTP, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="9f7d6-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="9f7d6-154">Протоколы, через которые API станет доступным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="9f7d6-155">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-155">This parameter is required.</span></span>
<span data-ttu-id="9f7d6-156">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-156">Default value is $null.</span></span>

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

### <span data-ttu-id="9f7d6-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="9f7d6-157">-ServiceUrl</span></span>
<span data-ttu-id="9f7d6-158">URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="9f7d6-159">Этот URL-адрес будет использоваться только для управления API Azure и не будет открыт.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="9f7d6-160">Должно содержать от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="9f7d6-161">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-161">This parameter is required.</span></span>

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

### <span data-ttu-id="9f7d6-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="9f7d6-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="9f7d6-163">Имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-163">Subscription key header name.</span></span>
<span data-ttu-id="9f7d6-164">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-164">This parameter is optional.</span></span>
<span data-ttu-id="9f7d6-165">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-165">Default value is $null.</span></span>

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

### <span data-ttu-id="9f7d6-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="9f7d6-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="9f7d6-167">Имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="9f7d6-168">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-168">This parameter is optional.</span></span>
<span data-ttu-id="9f7d6-169">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-169">Default value is $null.</span></span>

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

### <span data-ttu-id="9f7d6-170">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f7d6-170">-Confirm</span></span>
<span data-ttu-id="9f7d6-171">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f7d6-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f7d6-172">-WhatIf</span></span>
<span data-ttu-id="9f7d6-173">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f7d6-174">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f7d6-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f7d6-175">CommonParameters</span></span>
<span data-ttu-id="9f7d6-176">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f7d6-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f7d6-177">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f7d6-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f7d6-178">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f7d6-178">INPUTS</span></span>

### <span data-ttu-id="9f7d6-179">System. String</span><span class="sxs-lookup"><span data-stu-id="9f7d6-179">System.String</span></span>

### <span data-ttu-id="9f7d6-180">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9f7d6-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9f7d6-181">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9f7d6-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="9f7d6-182">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9f7d6-182">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9f7d6-183">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="9f7d6-183">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="9f7d6-184">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9f7d6-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9f7d6-185">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f7d6-185">OUTPUTS</span></span>

### <span data-ttu-id="9f7d6-186">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9f7d6-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="9f7d6-187">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f7d6-187">NOTES</span></span>

## <span data-ttu-id="9f7d6-188">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f7d6-188">RELATED LINKS</span></span>

[<span data-ttu-id="9f7d6-189">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="9f7d6-189">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="9f7d6-190">New-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="9f7d6-190">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="9f7d6-191">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="9f7d6-191">Remove-AzureRmApiManagementApiRevision</span></span>](./Remove-AzureRmApiManagementApiRevision.md)
