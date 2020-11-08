---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 02a7a35f4498724266d4c352744169d733f5eeab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079237"
---
# <span data-ttu-id="b9d19-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b9d19-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="b9d19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9d19-102">SYNOPSIS</span></span>
<span data-ttu-id="b9d19-103">Изменяет API.</span><span class="sxs-lookup"><span data-stu-id="b9d19-103">Modifies an API.</span></span>

## <span data-ttu-id="b9d19-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9d19-104">SYNTAX</span></span>

### <span data-ttu-id="b9d19-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9d19-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9d19-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b9d19-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9d19-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9d19-107">DESCRIPTION</span></span>
<span data-ttu-id="b9d19-108">Командлет **Set-AzApiManagementApi** изменяет интерфейс API управления Azure API.</span><span class="sxs-lookup"><span data-stu-id="b9d19-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="b9d19-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9d19-109">EXAMPLES</span></span>

### <span data-ttu-id="b9d19-110">Пример 1: изменение API</span><span class="sxs-lookup"><span data-stu-id="b9d19-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="b9d19-111">Пример 2: Добавление API к существующему ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b9d19-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="b9d19-112">В этом примере добавляется API в существующий комплект API-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b9d19-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="b9d19-113">Пример 3: изменение серверного ServiceUrl, на котором указывает API</span><span class="sxs-lookup"><span data-stu-id="b9d19-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="b9d19-114">В этом примере показано, как обновить ServiceUrl, на который `echo-api` указывает указатель.</span><span class="sxs-lookup"><span data-stu-id="b9d19-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="b9d19-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9d19-115">PARAMETERS</span></span>

### <span data-ttu-id="b9d19-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b9d19-116">-ApiId</span></span>
<span data-ttu-id="b9d19-117">Указывает идентификатор API, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="b9d19-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="b9d19-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="b9d19-118">-AuthorizationScope</span></span>
<span data-ttu-id="b9d19-119">Указывает область действий OAuth.</span><span class="sxs-lookup"><span data-stu-id="b9d19-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="b9d19-120">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b9d19-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="b9d19-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="b9d19-121">-AuthorizationServerId</span></span>
<span data-ttu-id="b9d19-122">Указывает идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="b9d19-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="b9d19-123">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b9d19-123">The default value is $Null.</span></span>
<span data-ttu-id="b9d19-124">Если указан *AuthorizationScope* , необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b9d19-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="b9d19-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="b9d19-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="b9d19-126">Механизм сервера авторизации OpenId, с помощью которого токен доступа передается API-интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="b9d19-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="b9d19-127">Ссылка на http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="b9d19-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="b9d19-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b9d19-128">This parameter is optional.</span></span> <span data-ttu-id="b9d19-129">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="b9d19-129">Default value is $null.</span></span>

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

### <span data-ttu-id="b9d19-130">-Context</span><span class="sxs-lookup"><span data-stu-id="b9d19-130">-Context</span></span>
<span data-ttu-id="b9d19-131">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b9d19-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b9d19-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9d19-132">-DefaultProfile</span></span>
<span data-ttu-id="b9d19-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9d19-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9d19-134">-Описание</span><span class="sxs-lookup"><span data-stu-id="b9d19-134">-Description</span></span>
<span data-ttu-id="b9d19-135">Задает описание для веб-API.</span><span class="sxs-lookup"><span data-stu-id="b9d19-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="b9d19-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9d19-136">-InputObject</span></span>
<span data-ttu-id="b9d19-137">Экземпляр PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="b9d19-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="b9d19-138">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="b9d19-138">This parameter is required.</span></span>

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

### <span data-ttu-id="b9d19-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b9d19-139">-Name</span></span>
<span data-ttu-id="b9d19-140">Указывает имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="b9d19-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="b9d19-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="b9d19-141">-OpenIdProviderId</span></span>
<span data-ttu-id="b9d19-142">Идентификатор сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="b9d19-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="b9d19-143">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b9d19-143">This parameter is optional.</span></span> <span data-ttu-id="b9d19-144">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="b9d19-144">Default value is $null.</span></span> <span data-ttu-id="b9d19-145">Должен быть указан, если указан BearerTokenSendingMethods.</span><span class="sxs-lookup"><span data-stu-id="b9d19-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="b9d19-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9d19-146">-PassThru</span></span>
<span data-ttu-id="b9d19-147">PassThru</span><span class="sxs-lookup"><span data-stu-id="b9d19-147">passthru</span></span>

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

### <span data-ttu-id="b9d19-148">-Path</span><span class="sxs-lookup"><span data-stu-id="b9d19-148">-Path</span></span>
<span data-ttu-id="b9d19-149">Указывает путь веб-API, который является последней частью общедоступного URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="b9d19-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="b9d19-150">Этот URL-адрес используется клиентами API для отправки запросов веб-службе и должен содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="b9d19-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="b9d19-151">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b9d19-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="b9d19-152">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="b9d19-152">-Protocols</span></span>
<span data-ttu-id="b9d19-153">Указывает массив протоколов веб-API.</span><span class="sxs-lookup"><span data-stu-id="b9d19-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="b9d19-154">psdx_paramvalues HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b9d19-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="b9d19-155">Это веб-протоколы, в которых интерфейс API становится доступным.</span><span class="sxs-lookup"><span data-stu-id="b9d19-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="b9d19-156">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b9d19-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="b9d19-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="b9d19-157">-ServiceUrl</span></span>
<span data-ttu-id="b9d19-158">Адрес URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="b9d19-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="b9d19-159">Этот URL-адрес используется только службой управления API Azure и не сделан общедоступным.</span><span class="sxs-lookup"><span data-stu-id="b9d19-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="b9d19-160">URL-адрес должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="b9d19-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="b9d19-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="b9d19-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="b9d19-162">Указывает имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="b9d19-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="b9d19-163">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b9d19-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="b9d19-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="b9d19-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="b9d19-165">Указывает имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="b9d19-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="b9d19-166">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b9d19-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="b9d19-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="b9d19-167">-SubscriptionRequired</span></span>
<span data-ttu-id="b9d19-168">Пометка для принудительного применения SubscriptionRequired для запросов к API.</span><span class="sxs-lookup"><span data-stu-id="b9d19-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="b9d19-169">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b9d19-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="b9d19-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9d19-170">CommonParameters</span></span>
<span data-ttu-id="b9d19-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9d19-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9d19-172">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9d19-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9d19-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9d19-173">INPUTS</span></span>

### <span data-ttu-id="b9d19-174">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b9d19-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b9d19-175">System. String</span><span class="sxs-lookup"><span data-stu-id="b9d19-175">System.String</span></span>

### <span data-ttu-id="b9d19-176">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b9d19-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="b9d19-177">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="b9d19-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="b9d19-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b9d19-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b9d19-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9d19-179">OUTPUTS</span></span>

### <span data-ttu-id="b9d19-180">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b9d19-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="b9d19-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9d19-181">NOTES</span></span>

## <span data-ttu-id="b9d19-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9d19-182">RELATED LINKS</span></span>

[<span data-ttu-id="b9d19-183">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b9d19-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="b9d19-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b9d19-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="b9d19-185">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b9d19-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="b9d19-186">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b9d19-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="b9d19-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b9d19-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


