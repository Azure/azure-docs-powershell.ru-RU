---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 295551f9d4ddf751980ec81626e3714a37aa47a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565746"
---
# <span data-ttu-id="aabc9-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aabc9-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="aabc9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aabc9-102">SYNOPSIS</span></span>
<span data-ttu-id="aabc9-103">Создание API.</span><span class="sxs-lookup"><span data-stu-id="aabc9-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aabc9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aabc9-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aabc9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aabc9-105">DESCRIPTION</span></span>
<span data-ttu-id="aabc9-106">Командлет **New-AzureRmApiManagementApi** создает API управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="aabc9-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="aabc9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aabc9-107">EXAMPLES</span></span>

### <span data-ttu-id="aabc9-108">Пример 1: создание API</span><span class="sxs-lookup"><span data-stu-id="aabc9-108">Example 1: Create an API</span></span>
```
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="aabc9-109">Эта команда создает API с именем EchoApi и указанным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="aabc9-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="aabc9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aabc9-110">PARAMETERS</span></span>

### <span data-ttu-id="aabc9-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="aabc9-111">-ApiId</span></span>
<span data-ttu-id="aabc9-112">Указывает идентификатор создаваемого API.</span><span class="sxs-lookup"><span data-stu-id="aabc9-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="aabc9-113">Если этот параметр не указан, этот командлет создаст идентификатор.</span><span class="sxs-lookup"><span data-stu-id="aabc9-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="aabc9-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="aabc9-114">-AuthorizationScope</span></span>
<span data-ttu-id="aabc9-115">Указывает область действий OAuth.</span><span class="sxs-lookup"><span data-stu-id="aabc9-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="aabc9-116">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="aabc9-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="aabc9-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="aabc9-117">-AuthorizationServerId</span></span>
<span data-ttu-id="aabc9-118">Указывает идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="aabc9-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="aabc9-119">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="aabc9-119">The default value is $Null.</span></span>
<span data-ttu-id="aabc9-120">Если указан *AuthorizationScope* , необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="aabc9-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="aabc9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="aabc9-121">-Context</span></span>
<span data-ttu-id="aabc9-122">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="aabc9-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="aabc9-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="aabc9-123">-Description</span></span>
<span data-ttu-id="aabc9-124">Задает описание для веб-API.</span><span class="sxs-lookup"><span data-stu-id="aabc9-124">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="aabc9-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aabc9-125">-Name</span></span>
<span data-ttu-id="aabc9-126">Указывает имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="aabc9-126">Specifies the name of the web API.</span></span>
<span data-ttu-id="aabc9-127">Это общедоступное имя API, которое отображается на порталах разработчиков и администраторов.</span><span class="sxs-lookup"><span data-stu-id="aabc9-127">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="aabc9-128">-Path</span><span class="sxs-lookup"><span data-stu-id="aabc9-128">-Path</span></span>
<span data-ttu-id="aabc9-129">Указывает путь веб-API, который является последней частью общедоступного URL-адреса API и соответствует полю суффикса URL-адреса Web API на портале администрирования.</span><span class="sxs-lookup"><span data-stu-id="aabc9-129">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="aabc9-130">Этот URL-адрес используется клиентами API для отправки запросов веб-службе и должен содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="aabc9-130">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="aabc9-131">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="aabc9-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="aabc9-132">-ProductId</span><span class="sxs-lookup"><span data-stu-id="aabc9-132">-ProductIds</span></span>
<span data-ttu-id="aabc9-133">Указывает массив идентификаторов продуктов, к которому нужно добавить новый API.</span><span class="sxs-lookup"><span data-stu-id="aabc9-133">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="aabc9-134">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="aabc9-134">-Protocols</span></span>
<span data-ttu-id="aabc9-135">Указывает массив протоколов веб-API.</span><span class="sxs-lookup"><span data-stu-id="aabc9-135">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="aabc9-136">Допустимые значения: HTTP, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="aabc9-136">Valid values are http, https.</span></span>
<span data-ttu-id="aabc9-137">Это веб-протоколы, в которых интерфейс API становится доступным.</span><span class="sxs-lookup"><span data-stu-id="aabc9-137">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="aabc9-138">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="aabc9-138">The default value is $Null.</span></span>

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

### <span data-ttu-id="aabc9-139">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="aabc9-139">-ServiceUrl</span></span>
<span data-ttu-id="aabc9-140">Адрес URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="aabc9-140">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="aabc9-141">Этот URL-адрес используется только службой управления API Azure и не сделан общедоступным.</span><span class="sxs-lookup"><span data-stu-id="aabc9-141">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="aabc9-142">URL-адрес должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="aabc9-142">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="aabc9-143">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="aabc9-143">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="aabc9-144">Задает имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="aabc9-144">Specifies the subscription key header name.</span></span>
<span data-ttu-id="aabc9-145">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="aabc9-145">The default value is $Null.</span></span>

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

### <span data-ttu-id="aabc9-146">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="aabc9-146">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="aabc9-147">Указывает имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="aabc9-147">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="aabc9-148">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="aabc9-148">The default value is $Null.</span></span>

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

### <span data-ttu-id="aabc9-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aabc9-149">-DefaultProfile</span></span>
<span data-ttu-id="aabc9-150">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aabc9-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aabc9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aabc9-151">CommonParameters</span></span>
<span data-ttu-id="aabc9-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aabc9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aabc9-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aabc9-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aabc9-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aabc9-154">INPUTS</span></span>

## <span data-ttu-id="aabc9-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aabc9-155">OUTPUTS</span></span>

### <span data-ttu-id="aabc9-156">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aabc9-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="aabc9-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="aabc9-157">NOTES</span></span>

## <span data-ttu-id="aabc9-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aabc9-158">RELATED LINKS</span></span>

[<span data-ttu-id="aabc9-159">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aabc9-159">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="aabc9-160">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aabc9-160">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="aabc9-161">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aabc9-161">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="aabc9-162">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aabc9-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="aabc9-163">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="aabc9-163">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


