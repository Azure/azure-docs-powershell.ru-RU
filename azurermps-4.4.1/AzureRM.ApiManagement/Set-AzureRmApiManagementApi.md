---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 4c9dc60ad1c531a5da9f32abc0090475c32a7ad5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568351"
---
# <span data-ttu-id="55e7d-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="55e7d-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="55e7d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="55e7d-103">Изменяет API.</span><span class="sxs-lookup"><span data-stu-id="55e7d-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55e7d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55e7d-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55e7d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55e7d-105">DESCRIPTION</span></span>
<span data-ttu-id="55e7d-106">Командлет **Set-AzureRmApiManagementApi** изменяет интерфейс API управления Azure API.</span><span class="sxs-lookup"><span data-stu-id="55e7d-106">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="55e7d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55e7d-107">EXAMPLES</span></span>

### <span data-ttu-id="55e7d-108">Пример 1. изменение API</span><span class="sxs-lookup"><span data-stu-id="55e7d-108">Example 1 Modify an API</span></span>
```
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="55e7d-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55e7d-109">PARAMETERS</span></span>

### <span data-ttu-id="55e7d-110">-ApiId</span><span class="sxs-lookup"><span data-stu-id="55e7d-110">-ApiId</span></span>
<span data-ttu-id="55e7d-111">Указывает идентификатор API, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="55e7d-111">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="55e7d-112">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="55e7d-112">-AuthorizationScope</span></span>
<span data-ttu-id="55e7d-113">Указывает область действий OAuth.</span><span class="sxs-lookup"><span data-stu-id="55e7d-113">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="55e7d-114">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="55e7d-114">The default value is $Null.</span></span>

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

### <span data-ttu-id="55e7d-115">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="55e7d-115">-AuthorizationServerId</span></span>
<span data-ttu-id="55e7d-116">Указывает идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="55e7d-116">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="55e7d-117">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="55e7d-117">The default value is $Null.</span></span>
<span data-ttu-id="55e7d-118">Если указан *AuthorizationScope* , необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="55e7d-118">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="55e7d-119">-Context</span><span class="sxs-lookup"><span data-stu-id="55e7d-119">-Context</span></span>
<span data-ttu-id="55e7d-120">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="55e7d-120">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55e7d-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="55e7d-121">-Description</span></span>
<span data-ttu-id="55e7d-122">Задает описание для веб-API.</span><span class="sxs-lookup"><span data-stu-id="55e7d-122">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="55e7d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="55e7d-123">-Name</span></span>
<span data-ttu-id="55e7d-124">Указывает имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="55e7d-124">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="55e7d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55e7d-125">-PassThru</span></span>
<span data-ttu-id="55e7d-126">PassThru</span><span class="sxs-lookup"><span data-stu-id="55e7d-126">passthru</span></span>

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

### <span data-ttu-id="55e7d-127">-Path</span><span class="sxs-lookup"><span data-stu-id="55e7d-127">-Path</span></span>
<span data-ttu-id="55e7d-128">Указывает путь веб-API, который является последней частью общедоступного URL-адреса API.</span><span class="sxs-lookup"><span data-stu-id="55e7d-128">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="55e7d-129">Этот URL-адрес используется клиентами API для отправки запросов веб-службе и должен содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="55e7d-129">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="55e7d-130">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="55e7d-130">The default value is $Null.</span></span>

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

### <span data-ttu-id="55e7d-131">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="55e7d-131">-Protocols</span></span>
<span data-ttu-id="55e7d-132">Указывает массив протоколов веб-API.</span><span class="sxs-lookup"><span data-stu-id="55e7d-132">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="55e7d-133">psdx_paramvalues HTTP и HTTPS.</span><span class="sxs-lookup"><span data-stu-id="55e7d-133">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="55e7d-134">Это веб-протоколы, в которых интерфейс API становится доступным.</span><span class="sxs-lookup"><span data-stu-id="55e7d-134">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="55e7d-135">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="55e7d-135">The default value is $Null.</span></span>

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

### <span data-ttu-id="55e7d-136">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="55e7d-136">-ServiceUrl</span></span>
<span data-ttu-id="55e7d-137">Адрес URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="55e7d-137">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="55e7d-138">Этот URL-адрес используется только службой управления API Azure и не сделан общедоступным.</span><span class="sxs-lookup"><span data-stu-id="55e7d-138">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="55e7d-139">URL-адрес должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="55e7d-139">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="55e7d-140">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="55e7d-140">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="55e7d-141">Указывает имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="55e7d-141">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="55e7d-142">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="55e7d-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="55e7d-143">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="55e7d-143">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="55e7d-144">Указывает имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="55e7d-144">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="55e7d-145">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="55e7d-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="55e7d-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e7d-146">-DefaultProfile</span></span>
<span data-ttu-id="55e7d-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55e7d-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55e7d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e7d-148">CommonParameters</span></span>
<span data-ttu-id="55e7d-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55e7d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e7d-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55e7d-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e7d-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55e7d-151">INPUTS</span></span>

## <span data-ttu-id="55e7d-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55e7d-152">OUTPUTS</span></span>

### <span data-ttu-id="55e7d-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="55e7d-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="55e7d-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="55e7d-154">NOTES</span></span>

## <span data-ttu-id="55e7d-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55e7d-155">RELATED LINKS</span></span>

[<span data-ttu-id="55e7d-156">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="55e7d-156">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="55e7d-157">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="55e7d-157">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="55e7d-158">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="55e7d-158">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="55e7d-159">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="55e7d-159">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="55e7d-160">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="55e7d-160">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


