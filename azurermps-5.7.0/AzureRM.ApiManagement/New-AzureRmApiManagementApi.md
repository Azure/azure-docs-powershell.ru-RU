---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 75a6dbf480e8b2f2f3d9f7524db4e57e5ed88f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734494"
---
# <span data-ttu-id="b7981-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b7981-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="b7981-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7981-102">SYNOPSIS</span></span>
<span data-ttu-id="b7981-103">Создание API.</span><span class="sxs-lookup"><span data-stu-id="b7981-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7981-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7981-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7981-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7981-105">DESCRIPTION</span></span>
<span data-ttu-id="b7981-106">Командлет **New-AzureRmApiManagementApi** создает API управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="b7981-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="b7981-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7981-107">EXAMPLES</span></span>

### <span data-ttu-id="b7981-108">Пример 1: создание API</span><span class="sxs-lookup"><span data-stu-id="b7981-108">Example 1: Create an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="b7981-109">Эта команда создает API с именем EchoApi и указанным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="b7981-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="b7981-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7981-110">PARAMETERS</span></span>

### <span data-ttu-id="b7981-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b7981-111">-ApiId</span></span>
<span data-ttu-id="b7981-112">Указывает идентификатор создаваемого API.</span><span class="sxs-lookup"><span data-stu-id="b7981-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="b7981-113">Если этот параметр не указан, этот командлет создаст идентификатор.</span><span class="sxs-lookup"><span data-stu-id="b7981-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="b7981-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="b7981-114">-AuthorizationScope</span></span>
<span data-ttu-id="b7981-115">Указывает область действий OAuth.</span><span class="sxs-lookup"><span data-stu-id="b7981-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="b7981-116">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b7981-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="b7981-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="b7981-117">-AuthorizationServerId</span></span>
<span data-ttu-id="b7981-118">Указывает идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="b7981-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="b7981-119">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b7981-119">The default value is $Null.</span></span>
<span data-ttu-id="b7981-120">Если указан *AuthorizationScope* , необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b7981-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="b7981-121">-Context</span><span class="sxs-lookup"><span data-stu-id="b7981-121">-Context</span></span>
<span data-ttu-id="b7981-122">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b7981-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b7981-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7981-123">-DefaultProfile</span></span>
<span data-ttu-id="b7981-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7981-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b7981-125">-Описание</span><span class="sxs-lookup"><span data-stu-id="b7981-125">-Description</span></span>
<span data-ttu-id="b7981-126">Задает описание для веб-API.</span><span class="sxs-lookup"><span data-stu-id="b7981-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="b7981-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7981-127">-Name</span></span>
<span data-ttu-id="b7981-128">Указывает имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="b7981-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="b7981-129">Это общедоступное имя API, которое отображается на порталах разработчиков и администраторов.</span><span class="sxs-lookup"><span data-stu-id="b7981-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="b7981-130">-Path</span><span class="sxs-lookup"><span data-stu-id="b7981-130">-Path</span></span>
<span data-ttu-id="b7981-131">Указывает путь веб-API, который является последней частью общедоступного URL-адреса API и соответствует полю суффикса URL-адреса Web API на портале администрирования.</span><span class="sxs-lookup"><span data-stu-id="b7981-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="b7981-132">Этот URL-адрес используется клиентами API для отправки запросов веб-службе и должен содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="b7981-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="b7981-133">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b7981-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="b7981-134">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b7981-134">-ProductIds</span></span>
<span data-ttu-id="b7981-135">Указывает массив идентификаторов продуктов, к которому нужно добавить новый API.</span><span class="sxs-lookup"><span data-stu-id="b7981-135">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7981-136">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="b7981-136">-Protocols</span></span>
<span data-ttu-id="b7981-137">Указывает массив протоколов веб-API.</span><span class="sxs-lookup"><span data-stu-id="b7981-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="b7981-138">Допустимые значения: HTTP, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b7981-138">Valid values are http, https.</span></span>
<span data-ttu-id="b7981-139">Это веб-протоколы, в которых интерфейс API становится доступным.</span><span class="sxs-lookup"><span data-stu-id="b7981-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="b7981-140">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b7981-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="b7981-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="b7981-141">-ServiceUrl</span></span>
<span data-ttu-id="b7981-142">Адрес URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="b7981-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="b7981-143">Этот URL-адрес используется только службой управления API Azure и не сделан общедоступным.</span><span class="sxs-lookup"><span data-stu-id="b7981-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="b7981-144">URL-адрес должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="b7981-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="b7981-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="b7981-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="b7981-146">Задает имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="b7981-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="b7981-147">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b7981-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="b7981-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="b7981-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="b7981-149">Указывает имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="b7981-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="b7981-150">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="b7981-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="b7981-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7981-151">CommonParameters</span></span>
<span data-ttu-id="b7981-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7981-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7981-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7981-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7981-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7981-154">INPUTS</span></span>

### <span data-ttu-id="b7981-155">Ничего</span><span class="sxs-lookup"><span data-stu-id="b7981-155">None</span></span>
<span data-ttu-id="b7981-156">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b7981-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7981-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7981-157">OUTPUTS</span></span>

### <span data-ttu-id="b7981-158">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b7981-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="b7981-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7981-159">NOTES</span></span>

## <span data-ttu-id="b7981-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7981-160">RELATED LINKS</span></span>

[<span data-ttu-id="b7981-161">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b7981-161">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="b7981-162">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b7981-162">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="b7981-163">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b7981-163">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="b7981-164">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b7981-164">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="b7981-165">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="b7981-165">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


