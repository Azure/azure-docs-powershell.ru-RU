---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 02a7a35f4498724266d4c352744169d733f5eeab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412140"
---
# <span data-ttu-id="e6269-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e6269-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="e6269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6269-102">SYNOPSIS</span></span>
<span data-ttu-id="e6269-103">Изменяет API.</span><span class="sxs-lookup"><span data-stu-id="e6269-103">Modifies an API.</span></span>

## <span data-ttu-id="e6269-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e6269-104">SYNTAX</span></span>

### <span data-ttu-id="e6269-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6269-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6269-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e6269-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6269-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6269-107">DESCRIPTION</span></span>
<span data-ttu-id="e6269-108">**Cmdlet Set-AzApiManagementApi** изменяет API управления Azure API.</span><span class="sxs-lookup"><span data-stu-id="e6269-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="e6269-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e6269-109">EXAMPLES</span></span>

### <span data-ttu-id="e6269-110">Пример 1. Изменение API</span><span class="sxs-lookup"><span data-stu-id="e6269-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="e6269-111">Пример 2. Добавление API в существующий ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="e6269-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="e6269-112">В этом примере API добавляется в существующий набор версий API.</span><span class="sxs-lookup"><span data-stu-id="e6269-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="e6269-113">Пример 3. Изменение backend ServiceUrl, на который указывают API</span><span class="sxs-lookup"><span data-stu-id="e6269-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="e6269-114">В этом примере обновляется указатель `echo-api` ServiceUrl.</span><span class="sxs-lookup"><span data-stu-id="e6269-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="e6269-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6269-115">PARAMETERS</span></span>

### <span data-ttu-id="e6269-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e6269-116">-ApiId</span></span>
<span data-ttu-id="e6269-117">Определяет код изменяемого API.</span><span class="sxs-lookup"><span data-stu-id="e6269-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="e6269-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="e6269-118">-AuthorizationScope</span></span>
<span data-ttu-id="e6269-119">Определяет область операций OAuth.</span><span class="sxs-lookup"><span data-stu-id="e6269-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="e6269-120">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="e6269-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="e6269-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="e6269-121">-AuthorizationServerId</span></span>
<span data-ttu-id="e6269-122">Определяет идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="e6269-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="e6269-123">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="e6269-123">The default value is $Null.</span></span>
<span data-ttu-id="e6269-124">Этот параметр необходимо указать, *если задан параметр AuthorizationScope.*</span><span class="sxs-lookup"><span data-stu-id="e6269-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="e6269-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="e6269-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="e6269-126">Механизм сервера авторизации OpenId, с помощью которого маркер доступа передается в API.</span><span class="sxs-lookup"><span data-stu-id="e6269-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="e6269-127">Обратитесь к http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="e6269-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="e6269-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e6269-128">This parameter is optional.</span></span> <span data-ttu-id="e6269-129">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="e6269-129">Default value is $null.</span></span>

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

### <span data-ttu-id="e6269-130">-Контекст</span><span class="sxs-lookup"><span data-stu-id="e6269-130">-Context</span></span>
<span data-ttu-id="e6269-131">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="e6269-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e6269-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6269-132">-DefaultProfile</span></span>
<span data-ttu-id="e6269-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6269-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6269-134">-Description</span><span class="sxs-lookup"><span data-stu-id="e6269-134">-Description</span></span>
<span data-ttu-id="e6269-135">Описание веб-API.</span><span class="sxs-lookup"><span data-stu-id="e6269-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="e6269-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6269-136">-InputObject</span></span>
<span data-ttu-id="e6269-137">Экземпляр PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="e6269-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="e6269-138">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="e6269-138">This parameter is required.</span></span>

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

### <span data-ttu-id="e6269-139">-Name</span><span class="sxs-lookup"><span data-stu-id="e6269-139">-Name</span></span>
<span data-ttu-id="e6269-140">Указывает имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="e6269-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="e6269-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="e6269-141">-OpenIdProviderId</span></span>
<span data-ttu-id="e6269-142">Идентификатор сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="e6269-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="e6269-143">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e6269-143">This parameter is optional.</span></span> <span data-ttu-id="e6269-144">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="e6269-144">Default value is $null.</span></span> <span data-ttu-id="e6269-145">Должен быть указан, если указан BearerTokenSendingMethods.</span><span class="sxs-lookup"><span data-stu-id="e6269-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="e6269-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6269-146">-PassThru</span></span>
<span data-ttu-id="e6269-147">passthru</span><span class="sxs-lookup"><span data-stu-id="e6269-147">passthru</span></span>

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

### <span data-ttu-id="e6269-148">-Path</span><span class="sxs-lookup"><span data-stu-id="e6269-148">-Path</span></span>
<span data-ttu-id="e6269-149">Путь к веб-API, который является последней частью url-адреса API.</span><span class="sxs-lookup"><span data-stu-id="e6269-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="e6269-150">Этот URL-адрес используется пользователями API для отправки запросов веб-службе и должен иметь длину от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="e6269-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="e6269-151">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="e6269-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="e6269-152">-Protocols</span><span class="sxs-lookup"><span data-stu-id="e6269-152">-Protocols</span></span>
<span data-ttu-id="e6269-153">Определяет массив протоколов веб-API.</span><span class="sxs-lookup"><span data-stu-id="e6269-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="e6269-154">psdx_paramvalues http и https.</span><span class="sxs-lookup"><span data-stu-id="e6269-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="e6269-155">Это веб-протоколы, на которых будет доступен API.</span><span class="sxs-lookup"><span data-stu-id="e6269-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="e6269-156">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="e6269-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="e6269-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="e6269-157">-ServiceUrl</span></span>
<span data-ttu-id="e6269-158">Url-адрес веб-службы, которая предоставляет API.</span><span class="sxs-lookup"><span data-stu-id="e6269-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="e6269-159">Этот URL-адрес используется только службой управления Azure API и не является общедоступным.</span><span class="sxs-lookup"><span data-stu-id="e6269-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="e6269-160">URL-адрес должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="e6269-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="e6269-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="e6269-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="e6269-162">Указывает имя заглавного названия ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="e6269-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="e6269-163">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="e6269-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="e6269-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="e6269-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="e6269-165">Указывает имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="e6269-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="e6269-166">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="e6269-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="e6269-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="e6269-167">-SubscriptionRequired</span></span>
<span data-ttu-id="e6269-168">Флаг для принудительного использования SubscriptionRequired для запросов к Api.</span><span class="sxs-lookup"><span data-stu-id="e6269-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="e6269-169">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e6269-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="e6269-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6269-170">CommonParameters</span></span>
<span data-ttu-id="e6269-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6269-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6269-172">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6269-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6269-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6269-173">INPUTS</span></span>

### <span data-ttu-id="e6269-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e6269-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e6269-175">System.String</span><span class="sxs-lookup"><span data-stu-id="e6269-175">System.String</span></span>

### <span data-ttu-id="e6269-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e6269-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="e6269-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="e6269-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="e6269-178">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e6269-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e6269-179">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6269-179">OUTPUTS</span></span>

### <span data-ttu-id="e6269-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e6269-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="e6269-181">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e6269-181">NOTES</span></span>

## <span data-ttu-id="e6269-182">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6269-182">RELATED LINKS</span></span>

[<span data-ttu-id="e6269-183">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e6269-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="e6269-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e6269-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="e6269-185">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e6269-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="e6269-186">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e6269-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="e6269-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e6269-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


