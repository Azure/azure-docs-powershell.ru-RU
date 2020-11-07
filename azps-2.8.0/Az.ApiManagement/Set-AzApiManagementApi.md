---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 973dc9bac629ee9a82b7624053f689bf7884fd8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727953"
---
# <span data-ttu-id="267c3-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="267c3-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="267c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="267c3-102">SYNOPSIS</span></span>
<span data-ttu-id="267c3-103">Изменяет API.</span><span class="sxs-lookup"><span data-stu-id="267c3-103">Modifies an API.</span></span>

## <span data-ttu-id="267c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="267c3-104">SYNTAX</span></span>

### <span data-ttu-id="267c3-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="267c3-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="267c3-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="267c3-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="267c3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="267c3-107">DESCRIPTION</span></span>
<span data-ttu-id="267c3-108">Командлет **Set-AzApiManagementApi** изменяет интерфейс API управления Azure API.</span><span class="sxs-lookup"><span data-stu-id="267c3-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="267c3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="267c3-109">EXAMPLES</span></span>

### <span data-ttu-id="267c3-110">Пример 1. изменение API</span><span class="sxs-lookup"><span data-stu-id="267c3-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="267c3-111">Пример 2. Добавление API в существующий ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="267c3-111">Example 2 Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```
<span data-ttu-id="267c3-112">В этом примере добавляется API в существующий комплект API-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="267c3-112">This example adds an API to an existing API Version Set</span></span>

## <span data-ttu-id="267c3-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="267c3-113">PARAMETERS</span></span>

### <span data-ttu-id="267c3-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="267c3-114">-ApiId</span></span>
<span data-ttu-id="267c3-115">Указывает идентификатор API, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="267c3-115">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="267c3-116">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="267c3-116">-AuthorizationScope</span></span>
<span data-ttu-id="267c3-117">Указывает область действий OAuth.</span><span class="sxs-lookup"><span data-stu-id="267c3-117">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="267c3-118">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="267c3-118">The default value is $Null.</span></span>

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

### <span data-ttu-id="267c3-119">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="267c3-119">-AuthorizationServerId</span></span>
<span data-ttu-id="267c3-120">Указывает идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="267c3-120">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="267c3-121">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="267c3-121">The default value is $Null.</span></span>
<span data-ttu-id="267c3-122">Если указан *AuthorizationScope* , необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="267c3-122">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="267c3-123">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="267c3-123">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="267c3-124">Механизм сервера авторизации OpenId, с помощью которого токен доступа передается API-интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="267c3-124">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="267c3-125">Ссылка на http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="267c3-125">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="267c3-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="267c3-126">This parameter is optional.</span></span> <span data-ttu-id="267c3-127">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="267c3-127">Default value is $null.</span></span>

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

### <span data-ttu-id="267c3-128">-Context</span><span class="sxs-lookup"><span data-stu-id="267c3-128">-Context</span></span>
<span data-ttu-id="267c3-129">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="267c3-129">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="267c3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="267c3-130">-DefaultProfile</span></span>
<span data-ttu-id="267c3-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="267c3-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="267c3-132">-Описание</span><span class="sxs-lookup"><span data-stu-id="267c3-132">-Description</span></span>
<span data-ttu-id="267c3-133">Задает описание для веб-API.</span><span class="sxs-lookup"><span data-stu-id="267c3-133">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="267c3-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="267c3-134">-InputObject</span></span>
<span data-ttu-id="267c3-135">Экземпляр PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="267c3-135">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="267c3-136">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="267c3-136">This parameter is required.</span></span>

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

### <span data-ttu-id="267c3-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="267c3-137">-Name</span></span>
<span data-ttu-id="267c3-138">Указывает имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="267c3-138">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="267c3-139">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="267c3-139">-OpenIdProviderId</span></span>
<span data-ttu-id="267c3-140">Идентификатор сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="267c3-140">OpenId authorization server identifier.</span></span> <span data-ttu-id="267c3-141">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="267c3-141">This parameter is optional.</span></span> <span data-ttu-id="267c3-142">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="267c3-142">Default value is $null.</span></span> <span data-ttu-id="267c3-143">Должен быть указан, если указан BearerTokenSendingMethods.</span><span class="sxs-lookup"><span data-stu-id="267c3-143">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="267c3-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="267c3-144">-PassThru</span></span>
<span data-ttu-id="267c3-145">PassThru</span><span class="sxs-lookup"><span data-stu-id="267c3-145">passthru</span></span>

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

### <span data-ttu-id="267c3-146">-Path</span><span class="sxs-lookup"><span data-stu-id="267c3-146">-Path</span></span>
<span data-ttu-id="267c3-147">Указывает путь веб-API, который является последней частью общедоступного URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="267c3-147">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="267c3-148">Этот URL-адрес используется клиентами API для отправки запросов веб-службе и должен содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="267c3-148">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="267c3-149">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="267c3-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="267c3-150">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="267c3-150">-Protocols</span></span>
<span data-ttu-id="267c3-151">Указывает массив протоколов веб-API.</span><span class="sxs-lookup"><span data-stu-id="267c3-151">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="267c3-152">psdx_paramvalues HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="267c3-152">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="267c3-153">Это веб-протоколы, в которых интерфейс API становится доступным.</span><span class="sxs-lookup"><span data-stu-id="267c3-153">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="267c3-154">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="267c3-154">The default value is $Null.</span></span>

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

### <span data-ttu-id="267c3-155">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="267c3-155">-ServiceUrl</span></span>
<span data-ttu-id="267c3-156">Адрес URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="267c3-156">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="267c3-157">Этот URL-адрес используется только службой управления API Azure и не сделан общедоступным.</span><span class="sxs-lookup"><span data-stu-id="267c3-157">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="267c3-158">URL-адрес должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="267c3-158">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="267c3-159">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="267c3-159">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="267c3-160">Указывает имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="267c3-160">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="267c3-161">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="267c3-161">The default value is $Null.</span></span>

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

### <span data-ttu-id="267c3-162">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="267c3-162">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="267c3-163">Указывает имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="267c3-163">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="267c3-164">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="267c3-164">The default value is $Null.</span></span>

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

### <span data-ttu-id="267c3-165">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="267c3-165">-SubscriptionRequired</span></span>
<span data-ttu-id="267c3-166">Пометка для принудительного применения SubscriptionRequired для запросов к API.</span><span class="sxs-lookup"><span data-stu-id="267c3-166">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="267c3-167">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="267c3-167">This parameter is optional.</span></span>

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

### <span data-ttu-id="267c3-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="267c3-168">CommonParameters</span></span>
<span data-ttu-id="267c3-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="267c3-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="267c3-170">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="267c3-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="267c3-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="267c3-171">INPUTS</span></span>

### <span data-ttu-id="267c3-172">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="267c3-172">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="267c3-173">System. String</span><span class="sxs-lookup"><span data-stu-id="267c3-173">System.String</span></span>

### <span data-ttu-id="267c3-174">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="267c3-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="267c3-175">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="267c3-175">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="267c3-176">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="267c3-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="267c3-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="267c3-177">OUTPUTS</span></span>

### <span data-ttu-id="267c3-178">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="267c3-178">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="267c3-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="267c3-179">NOTES</span></span>

## <span data-ttu-id="267c3-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="267c3-180">RELATED LINKS</span></span>

[<span data-ttu-id="267c3-181">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="267c3-181">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="267c3-182">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="267c3-182">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="267c3-183">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="267c3-183">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="267c3-184">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="267c3-184">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="267c3-185">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="267c3-185">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


