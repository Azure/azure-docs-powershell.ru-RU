---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 43793ef7d1d3f9a4e5e63687e1eaf785d237e86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720120"
---
# <span data-ttu-id="2e6d1-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e6d1-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="2e6d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e6d1-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6d1-103">Создание API.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-103">Creates an API.</span></span>

## <span data-ttu-id="2e6d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e6d1-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e6d1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e6d1-105">DESCRIPTION</span></span>
<span data-ttu-id="2e6d1-106">Командлет **New-AzApiManagementApi** создает API управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="2e6d1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e6d1-107">EXAMPLES</span></span>

### <span data-ttu-id="2e6d1-108">Пример 1: создание API</span><span class="sxs-lookup"><span data-stu-id="2e6d1-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="2e6d1-109">Эта команда создает API с именем EchoApi и указанным URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="2e6d1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e6d1-110">PARAMETERS</span></span>

### <span data-ttu-id="2e6d1-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2e6d1-111">-ApiId</span></span>
<span data-ttu-id="2e6d1-112">Указывает идентификатор создаваемого API.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="2e6d1-113">Если этот параметр не указан, этот командлет создаст идентификатор.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="2e6d1-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="2e6d1-114">-AuthorizationScope</span></span>
<span data-ttu-id="2e6d1-115">Указывает область действий OAuth.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="2e6d1-116">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="2e6d1-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="2e6d1-117">-AuthorizationServerId</span></span>
<span data-ttu-id="2e6d1-118">Указывает идентификатор сервера авторизации OAuth.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="2e6d1-119">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-119">The default value is $Null.</span></span>
<span data-ttu-id="2e6d1-120">Если указан *AuthorizationScope* , необходимо указать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="2e6d1-121">-Context</span><span class="sxs-lookup"><span data-stu-id="2e6d1-121">-Context</span></span>
<span data-ttu-id="2e6d1-122">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2e6d1-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2e6d1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6d1-123">-DefaultProfile</span></span>
<span data-ttu-id="2e6d1-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e6d1-125">-Описание</span><span class="sxs-lookup"><span data-stu-id="2e6d1-125">-Description</span></span>
<span data-ttu-id="2e6d1-126">Задает описание для веб-API.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="2e6d1-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e6d1-127">-Name</span></span>
<span data-ttu-id="2e6d1-128">Указывает имя веб-API.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="2e6d1-129">Это общедоступное имя API, которое отображается на порталах разработчиков и администраторов.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="2e6d1-130">-Path</span><span class="sxs-lookup"><span data-stu-id="2e6d1-130">-Path</span></span>
<span data-ttu-id="2e6d1-131">Указывает путь веб-API, который является последней частью общедоступного URL-адреса API и соответствует полю суффикса URL-адреса Web API на портале администрирования.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="2e6d1-132">Этот URL-адрес используется клиентами API для отправки запросов веб-службе и должен содержать от 1 до 400 символов.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="2e6d1-133">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="2e6d1-134">-ProductId</span><span class="sxs-lookup"><span data-stu-id="2e6d1-134">-ProductIds</span></span>
<span data-ttu-id="2e6d1-135">Указывает массив идентификаторов продуктов, к которому нужно добавить новый API.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-135">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="2e6d1-136">-Протоколы</span><span class="sxs-lookup"><span data-stu-id="2e6d1-136">-Protocols</span></span>
<span data-ttu-id="2e6d1-137">Указывает массив протоколов веб-API.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="2e6d1-138">Допустимые значения: HTTP, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-138">Valid values are http, https.</span></span>
<span data-ttu-id="2e6d1-139">Это веб-протоколы, в которых интерфейс API становится доступным.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="2e6d1-140">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="2e6d1-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="2e6d1-141">-ServiceUrl</span></span>
<span data-ttu-id="2e6d1-142">Адрес URL веб-службы, предоставляющей API.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="2e6d1-143">Этот URL-адрес используется только службой управления API Azure и не сделан общедоступным.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="2e6d1-144">URL-адрес должен иметь длину от 1 до 2000 символов.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="2e6d1-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="2e6d1-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="2e6d1-146">Задает имя заголовка ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="2e6d1-147">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="2e6d1-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="2e6d1-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="2e6d1-149">Указывает имя параметра строки запроса ключа подписки.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="2e6d1-150">Значение по умолчанию — $Null.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="2e6d1-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6d1-151">CommonParameters</span></span>
<span data-ttu-id="2e6d1-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e6d1-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6d1-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e6d1-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6d1-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e6d1-154">INPUTS</span></span>

### <span data-ttu-id="2e6d1-155">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e6d1-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2e6d1-156">System. String</span><span class="sxs-lookup"><span data-stu-id="2e6d1-156">System.String</span></span>

### <span data-ttu-id="2e6d1-157">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="2e6d1-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="2e6d1-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="2e6d1-158">System.String[]</span></span>

## <span data-ttu-id="2e6d1-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e6d1-159">OUTPUTS</span></span>

### <span data-ttu-id="2e6d1-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e6d1-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="2e6d1-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e6d1-161">NOTES</span></span>

## <span data-ttu-id="2e6d1-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e6d1-162">RELATED LINKS</span></span>

[<span data-ttu-id="2e6d1-163">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e6d1-163">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="2e6d1-164">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e6d1-164">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="2e6d1-165">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e6d1-165">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="2e6d1-166">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e6d1-166">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="2e6d1-167">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="2e6d1-167">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


