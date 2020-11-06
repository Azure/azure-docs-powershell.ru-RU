---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: 545c1f57d269b8cdb36e006a07c754811e0f2b04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565723"
---
# <span data-ttu-id="132e5-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="132e5-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="132e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="132e5-102">SYNOPSIS</span></span>
<span data-ttu-id="132e5-103">Создает операцию управления API.</span><span class="sxs-lookup"><span data-stu-id="132e5-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="132e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="132e5-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-OperationId <String>]
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="132e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="132e5-105">DESCRIPTION</span></span>
<span data-ttu-id="132e5-106">Командлет **New-AzureRmApiManagementOperation** создает операцию API.</span><span class="sxs-lookup"><span data-stu-id="132e5-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="132e5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="132e5-107">EXAMPLES</span></span>

### <span data-ttu-id="132e5-108">Пример 1: создание операции управления API</span><span class="sxs-lookup"><span data-stu-id="132e5-108">Example 1: Create an API management operation</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="132e5-109">Эта команда создает операцию управления API.</span><span class="sxs-lookup"><span data-stu-id="132e5-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="132e5-110">Пример 2: создание операции управления API с данными запроса и ответа</span><span class="sxs-lookup"><span data-stu-id="132e5-110">Example 2: Create an API management operation with request and response details</span></span>
```
PS C:\>$RID = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$RID.Name = "RID"
$RID.Description = "Resource identifier"
$RID.Type = "string"
$Query = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Query.Name = "query"
$Query.Description = "Query string"
$Query.Type = 'string'
$Request = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
$Request.Description = "Create/update resource request"
$DummyQp = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$DummyQp.Name = 'dummy'
$DummyQp.Type = 'string'
$DummyQp.Required = $FALSE
$Request.QueryParameters = @($DummyQp)
$Header = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Header.Name = 'x-custom-header'
$Header.Type = 'string'
$Request.Headers = @($Header)
$RequestRepresentation = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRepresentation
$RequestRepresentation.ContentType = 'application/json'
$RequestRepresentation.Sample = '{ "propName": "propValue" }'
$Request.Representations = @($requestRepresentation)
$Response = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse
$Response.StatusCode = 204
New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="132e5-111">В этом примере создается операция управления API с подробными сведениями о запросе и ответе.</span><span class="sxs-lookup"><span data-stu-id="132e5-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="132e5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="132e5-112">PARAMETERS</span></span>

### <span data-ttu-id="132e5-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="132e5-113">-ApiId</span></span>
<span data-ttu-id="132e5-114">Задает идентификатор операции управления API.</span><span class="sxs-lookup"><span data-stu-id="132e5-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="132e5-115">-Context</span><span class="sxs-lookup"><span data-stu-id="132e5-115">-Context</span></span>
<span data-ttu-id="132e5-116">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="132e5-116">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="132e5-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="132e5-117">-Description</span></span>
<span data-ttu-id="132e5-118">Задает описание новой операции API.</span><span class="sxs-lookup"><span data-stu-id="132e5-118">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="132e5-119">-Method</span><span class="sxs-lookup"><span data-stu-id="132e5-119">-Method</span></span>
<span data-ttu-id="132e5-120">Задает метод HTTP для новой операции управления API.</span><span class="sxs-lookup"><span data-stu-id="132e5-120">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="132e5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="132e5-121">-Name</span></span>
<span data-ttu-id="132e5-122">Указывает отображаемое имя для новой операции управления API.</span><span class="sxs-lookup"><span data-stu-id="132e5-122">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="132e5-123">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="132e5-123">-OperationId</span></span>
<span data-ttu-id="132e5-124">Задает идентификатор операции управления API.</span><span class="sxs-lookup"><span data-stu-id="132e5-124">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="132e5-125">-Request</span><span class="sxs-lookup"><span data-stu-id="132e5-125">-Request</span></span>
<span data-ttu-id="132e5-126">Задает данные для операции управления API.</span><span class="sxs-lookup"><span data-stu-id="132e5-126">Specifies the details of the API management operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="132e5-127">-Ответы</span><span class="sxs-lookup"><span data-stu-id="132e5-127">-Responses</span></span>
<span data-ttu-id="132e5-128">Указывает массив возможных ответов операций управления API.</span><span class="sxs-lookup"><span data-stu-id="132e5-128">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="132e5-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="132e5-129">-TemplateParameters</span></span>
<span data-ttu-id="132e5-130">Задает массив параметров, определенных в параметре *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="132e5-130">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="132e5-131">Если этот параметр не указан, на основе *UrlTemplate* будет создано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="132e5-131">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="132e5-132">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="132e5-132">-UrlTemplate</span></span>
<span data-ttu-id="132e5-133">Задает шаблон URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="132e5-133">Specifies the URL template.</span></span>

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

### <span data-ttu-id="132e5-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="132e5-134">-DefaultProfile</span></span>
<span data-ttu-id="132e5-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="132e5-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="132e5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="132e5-136">CommonParameters</span></span>
<span data-ttu-id="132e5-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="132e5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="132e5-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="132e5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="132e5-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="132e5-139">INPUTS</span></span>

## <span data-ttu-id="132e5-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="132e5-140">OUTPUTS</span></span>

### <span data-ttu-id="132e5-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="132e5-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="132e5-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="132e5-142">NOTES</span></span>

## <span data-ttu-id="132e5-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="132e5-143">RELATED LINKS</span></span>

[<span data-ttu-id="132e5-144">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="132e5-144">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="132e5-145">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="132e5-145">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="132e5-146">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="132e5-146">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


