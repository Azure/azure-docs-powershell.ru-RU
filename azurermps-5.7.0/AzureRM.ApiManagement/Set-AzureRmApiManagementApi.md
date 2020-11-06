---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 6ab29738f181f6fece9d3b4cd679496a9add9bc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566254"
---
# <span data-ttu-id="9b74e-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9b74e-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="9b74e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b74e-102">SYNOPSIS</span></span>
<span data-ttu-id="9b74e-103">Изменяет API.</span><span class="sxs-lookup"><span data-stu-id="9b74e-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b74e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b74e-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b74e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b74e-105">DESCRIPTION</span></span>
<span data-ttu-id="9b74e-106">Командлет **Set-AzureRmApiManagementApi** изменяет интерфейс API управления Azure API.</span><span class="sxs-lookup"><span data-stu-id="9b74e-106">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="9b74e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b74e-107">EXAMPLES</span></span>

### <span data-ttu-id="9b74e-108">Пример 1. изменение API</span><span class="sxs-lookup"><span data-stu-id="9b74e-108">Example 1 Modify an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="9b74e-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b74e-109">PARAMETERS</span></span>

### <span data-ttu-id="9b74e-110">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9b74e-110">-ApiId</span></span>
<span data-ttu-id="9b74e-111">Указывает идентификатор API, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="9b74e-111">Specifies the ID of the API to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b74e-112">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="9b74e-112">-AuthorizationScope</span></span>
<span data-ttu-id="9b74e-113">Указывает область действий OAuth.</span><span class="sxs-lookup"><span data-stu-id="9b74e-113">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="9b74e-114">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="9b74e-114">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b74e-115">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="9b74e-115">-AuthorizationServerId</span></span>
<span data-ttu-id="9b74e-116">Указывает идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="9b74e-116">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="9b74e-117">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="9b74e-117">The default value is $Null.</span></span>
<span data-ttu-id="9b74e-118">Если указан *AuthorizationScope* , необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9b74e-118">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b74e-119">-Context</span><span class="sxs-lookup"><span data-stu-id="9b74e-119">-Context</span></span>
<span data-ttu-id="9b74e-120">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9b74e-120">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b74e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b74e-121">-DefaultProfile</span></span>
<span data-ttu-id="9b74e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b74e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b74e-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="9b74e-123">-Description</span></span>
<span data-ttu-id="9b74e-124">Задает описание для веб-API.</span><span class="sxs-lookup"><span data-stu-id="9b74e-124">Specifies a description for the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b74e-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9b74e-125">-Name</span></span>
<span data-ttu-id="9b74e-126">Указывает имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="9b74e-126">Specifies the name of the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b74e-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b74e-127">-PassThru</span></span>
<span data-ttu-id="9b74e-128">PassThru</span><span class="sxs-lookup"><span data-stu-id="9b74e-128">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b74e-129">-Path</span><span class="sxs-lookup"><span data-stu-id="9b74e-129">-Path</span></span>
<span data-ttu-id="9b74e-130">Указывает путь веб-API, который является последней частью общедоступного URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="9b74e-130">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="9b74e-131">Этот URL-адрес используется клиентами API для отправки запросов веб-службе и должен содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="9b74e-131">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="9b74e-132">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="9b74e-132">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b74e-133">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="9b74e-133">-Protocols</span></span>
<span data-ttu-id="9b74e-134">Указывает массив протоколов веб-API.</span><span class="sxs-lookup"><span data-stu-id="9b74e-134">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="9b74e-135">psdx_paramvalues HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9b74e-135">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="9b74e-136">Это веб-протоколы, в которых интерфейс API становится доступным.</span><span class="sxs-lookup"><span data-stu-id="9b74e-136">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="9b74e-137">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="9b74e-137">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSchema[]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b74e-138">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="9b74e-138">-ServiceUrl</span></span>
<span data-ttu-id="9b74e-139">Адрес URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="9b74e-139">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="9b74e-140">Этот URL-адрес используется только службой управления API Azure и не сделан общедоступным.</span><span class="sxs-lookup"><span data-stu-id="9b74e-140">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="9b74e-141">URL-адрес должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="9b74e-141">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b74e-142">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="9b74e-142">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="9b74e-143">Указывает имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="9b74e-143">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="9b74e-144">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="9b74e-144">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b74e-145">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="9b74e-145">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="9b74e-146">Указывает имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="9b74e-146">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="9b74e-147">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="9b74e-147">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b74e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b74e-148">CommonParameters</span></span>
<span data-ttu-id="9b74e-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b74e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b74e-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b74e-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b74e-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b74e-151">INPUTS</span></span>

### <span data-ttu-id="9b74e-152">Ничего</span><span class="sxs-lookup"><span data-stu-id="9b74e-152">None</span></span>
<span data-ttu-id="9b74e-153">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9b74e-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9b74e-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b74e-154">OUTPUTS</span></span>

### <span data-ttu-id="9b74e-155">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9b74e-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="9b74e-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b74e-156">NOTES</span></span>

## <span data-ttu-id="9b74e-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b74e-157">RELATED LINKS</span></span>

[<span data-ttu-id="9b74e-158">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9b74e-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="9b74e-159">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9b74e-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="9b74e-160">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9b74e-160">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="9b74e-161">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9b74e-161">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="9b74e-162">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9b74e-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


