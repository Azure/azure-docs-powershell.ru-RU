---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 10df1034b414260cb618c7de0b31b8ad93d30d0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567319"
---
# <span data-ttu-id="5749f-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5749f-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="5749f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5749f-102">SYNOPSIS</span></span>
<span data-ttu-id="5749f-103">Изменяет API.</span><span class="sxs-lookup"><span data-stu-id="5749f-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5749f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5749f-104">SYNTAX</span></span>

### <span data-ttu-id="5749f-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5749f-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5749f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5749f-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5749f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5749f-107">DESCRIPTION</span></span>
<span data-ttu-id="5749f-108">Командлет **Set-AzureRmApiManagementApi** изменяет интерфейс API управления Azure API.</span><span class="sxs-lookup"><span data-stu-id="5749f-108">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="5749f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5749f-109">EXAMPLES</span></span>

### <span data-ttu-id="5749f-110">Пример 1. изменение API</span><span class="sxs-lookup"><span data-stu-id="5749f-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="5749f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5749f-111">PARAMETERS</span></span>

### <span data-ttu-id="5749f-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5749f-112">-ApiId</span></span>
<span data-ttu-id="5749f-113">Указывает идентификатор API, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="5749f-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="5749f-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="5749f-114">-AuthorizationScope</span></span>
<span data-ttu-id="5749f-115">Указывает область действий OAuth.</span><span class="sxs-lookup"><span data-stu-id="5749f-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="5749f-116">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="5749f-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="5749f-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="5749f-117">-AuthorizationServerId</span></span>
<span data-ttu-id="5749f-118">Указывает идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="5749f-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="5749f-119">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="5749f-119">The default value is $Null.</span></span>
<span data-ttu-id="5749f-120">Если указан *AuthorizationScope* , необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="5749f-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="5749f-121">-Context</span><span class="sxs-lookup"><span data-stu-id="5749f-121">-Context</span></span>
<span data-ttu-id="5749f-122">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5749f-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5749f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5749f-123">-DefaultProfile</span></span>
<span data-ttu-id="5749f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5749f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5749f-125">-Описание</span><span class="sxs-lookup"><span data-stu-id="5749f-125">-Description</span></span>
<span data-ttu-id="5749f-126">Задает описание для веб-API.</span><span class="sxs-lookup"><span data-stu-id="5749f-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="5749f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5749f-127">-InputObject</span></span>
<span data-ttu-id="5749f-128">Экземпляр PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="5749f-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="5749f-129">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="5749f-129">This parameter is required.</span></span>

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

### <span data-ttu-id="5749f-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5749f-130">-Name</span></span>
<span data-ttu-id="5749f-131">Указывает имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="5749f-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="5749f-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5749f-132">-PassThru</span></span>
<span data-ttu-id="5749f-133">PassThru</span><span class="sxs-lookup"><span data-stu-id="5749f-133">passthru</span></span>

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

### <span data-ttu-id="5749f-134">-Path</span><span class="sxs-lookup"><span data-stu-id="5749f-134">-Path</span></span>
<span data-ttu-id="5749f-135">Указывает путь веб-API, который является последней частью общедоступного URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="5749f-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="5749f-136">Этот URL-адрес используется клиентами API для отправки запросов веб-службе и должен содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="5749f-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="5749f-137">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="5749f-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="5749f-138">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="5749f-138">-Protocols</span></span>
<span data-ttu-id="5749f-139">Указывает массив протоколов веб-API.</span><span class="sxs-lookup"><span data-stu-id="5749f-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="5749f-140">psdx_paramvalues HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5749f-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="5749f-141">Это веб-протоколы, в которых интерфейс API становится доступным.</span><span class="sxs-lookup"><span data-stu-id="5749f-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="5749f-142">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="5749f-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="5749f-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="5749f-143">-ServiceUrl</span></span>
<span data-ttu-id="5749f-144">Адрес URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="5749f-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="5749f-145">Этот URL-адрес используется только службой управления API Azure и не сделан общедоступным.</span><span class="sxs-lookup"><span data-stu-id="5749f-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="5749f-146">URL-адрес должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="5749f-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="5749f-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="5749f-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="5749f-148">Указывает имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="5749f-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="5749f-149">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="5749f-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="5749f-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="5749f-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="5749f-151">Указывает имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="5749f-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="5749f-152">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="5749f-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="5749f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5749f-153">CommonParameters</span></span>
<span data-ttu-id="5749f-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5749f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5749f-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5749f-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5749f-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5749f-156">INPUTS</span></span>

### <span data-ttu-id="5749f-157">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5749f-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5749f-158">System. String</span><span class="sxs-lookup"><span data-stu-id="5749f-158">System.String</span></span>

### <span data-ttu-id="5749f-159">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5749f-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="5749f-160">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5749f-160">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5749f-161">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="5749f-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="5749f-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5749f-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5749f-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5749f-163">OUTPUTS</span></span>

### <span data-ttu-id="5749f-164">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5749f-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="5749f-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="5749f-165">NOTES</span></span>

## <span data-ttu-id="5749f-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5749f-166">RELATED LINKS</span></span>

[<span data-ttu-id="5749f-167">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5749f-167">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="5749f-168">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5749f-168">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="5749f-169">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5749f-169">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="5749f-170">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5749f-170">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="5749f-171">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5749f-171">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


