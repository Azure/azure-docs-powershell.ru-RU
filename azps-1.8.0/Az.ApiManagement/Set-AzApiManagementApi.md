---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 190dfb075e16b6b7eaaa0cb6fafd0145b3211654
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901609"
---
# <span data-ttu-id="0a941-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0a941-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="0a941-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a941-102">SYNOPSIS</span></span>
<span data-ttu-id="0a941-103">Изменяет API.</span><span class="sxs-lookup"><span data-stu-id="0a941-103">Modifies an API.</span></span>

## <span data-ttu-id="0a941-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a941-104">SYNTAX</span></span>

### <span data-ttu-id="0a941-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a941-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a941-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0a941-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a941-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a941-107">DESCRIPTION</span></span>
<span data-ttu-id="0a941-108">Командлет **Set-AzApiManagementApi** изменяет интерфейс API управления Azure API.</span><span class="sxs-lookup"><span data-stu-id="0a941-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="0a941-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a941-109">EXAMPLES</span></span>

### <span data-ttu-id="0a941-110">Пример 1. изменение API</span><span class="sxs-lookup"><span data-stu-id="0a941-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="0a941-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a941-111">PARAMETERS</span></span>

### <span data-ttu-id="0a941-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0a941-112">-ApiId</span></span>
<span data-ttu-id="0a941-113">Указывает идентификатор API, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="0a941-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="0a941-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="0a941-114">-AuthorizationScope</span></span>
<span data-ttu-id="0a941-115">Указывает область действий OAuth.</span><span class="sxs-lookup"><span data-stu-id="0a941-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="0a941-116">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="0a941-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="0a941-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="0a941-117">-AuthorizationServerId</span></span>
<span data-ttu-id="0a941-118">Указывает идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="0a941-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="0a941-119">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="0a941-119">The default value is $Null.</span></span>
<span data-ttu-id="0a941-120">Если указан *AuthorizationScope* , необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="0a941-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="0a941-121">-Context</span><span class="sxs-lookup"><span data-stu-id="0a941-121">-Context</span></span>
<span data-ttu-id="0a941-122">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0a941-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0a941-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a941-123">-DefaultProfile</span></span>
<span data-ttu-id="0a941-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a941-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a941-125">-Описание</span><span class="sxs-lookup"><span data-stu-id="0a941-125">-Description</span></span>
<span data-ttu-id="0a941-126">Задает описание для веб-API.</span><span class="sxs-lookup"><span data-stu-id="0a941-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="0a941-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a941-127">-InputObject</span></span>
<span data-ttu-id="0a941-128">Экземпляр PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="0a941-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="0a941-129">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="0a941-129">This parameter is required.</span></span>

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

### <span data-ttu-id="0a941-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a941-130">-Name</span></span>
<span data-ttu-id="0a941-131">Указывает имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="0a941-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="0a941-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a941-132">-PassThru</span></span>
<span data-ttu-id="0a941-133">PassThru</span><span class="sxs-lookup"><span data-stu-id="0a941-133">passthru</span></span>

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

### <span data-ttu-id="0a941-134">-Path</span><span class="sxs-lookup"><span data-stu-id="0a941-134">-Path</span></span>
<span data-ttu-id="0a941-135">Указывает путь веб-API, который является последней частью общедоступного URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="0a941-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="0a941-136">Этот URL-адрес используется клиентами API для отправки запросов веб-службе и должен содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="0a941-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="0a941-137">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="0a941-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="0a941-138">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="0a941-138">-Protocols</span></span>
<span data-ttu-id="0a941-139">Указывает массив протоколов веб-API.</span><span class="sxs-lookup"><span data-stu-id="0a941-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="0a941-140">psdx_paramvalues HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="0a941-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="0a941-141">Это веб-протоколы, в которых интерфейс API становится доступным.</span><span class="sxs-lookup"><span data-stu-id="0a941-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="0a941-142">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="0a941-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="0a941-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="0a941-143">-ServiceUrl</span></span>
<span data-ttu-id="0a941-144">Адрес URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="0a941-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="0a941-145">Этот URL-адрес используется только службой управления API Azure и не сделан общедоступным.</span><span class="sxs-lookup"><span data-stu-id="0a941-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="0a941-146">URL-адрес должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="0a941-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="0a941-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="0a941-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="0a941-148">Указывает имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="0a941-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="0a941-149">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="0a941-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="0a941-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="0a941-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="0a941-151">Указывает имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="0a941-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="0a941-152">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="0a941-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="0a941-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a941-153">CommonParameters</span></span>
<span data-ttu-id="0a941-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a941-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a941-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a941-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a941-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a941-156">INPUTS</span></span>

### <span data-ttu-id="0a941-157">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0a941-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0a941-158">System. String</span><span class="sxs-lookup"><span data-stu-id="0a941-158">System.String</span></span>

### <span data-ttu-id="0a941-159">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0a941-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="0a941-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="0a941-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="0a941-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0a941-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0a941-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a941-162">OUTPUTS</span></span>

### <span data-ttu-id="0a941-163">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0a941-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="0a941-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a941-164">NOTES</span></span>

## <span data-ttu-id="0a941-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a941-165">RELATED LINKS</span></span>

[<span data-ttu-id="0a941-166">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0a941-166">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="0a941-167">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0a941-167">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="0a941-168">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0a941-168">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="0a941-169">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0a941-169">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="0a941-170">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0a941-170">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


