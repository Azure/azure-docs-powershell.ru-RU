---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: 36560b23d9108ff1f8cd981abdb44a3c24f25402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557639"
---
# <span data-ttu-id="7f789-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="7f789-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="7f789-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f789-102">SYNOPSIS</span></span>
<span data-ttu-id="7f789-103">Создает операцию управления API.</span><span class="sxs-lookup"><span data-stu-id="7f789-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f789-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f789-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-OperationId <String>]
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f789-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f789-105">DESCRIPTION</span></span>
<span data-ttu-id="7f789-106">Командлет **New-AzureRmApiManagementOperation** создает операцию API.</span><span class="sxs-lookup"><span data-stu-id="7f789-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="7f789-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f789-107">EXAMPLES</span></span>

### <span data-ttu-id="7f789-108">Пример 1: создание операции управления API</span><span class="sxs-lookup"><span data-stu-id="7f789-108">Example 1: Create an API management operation</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="7f789-109">Эта команда создает операцию управления API.</span><span class="sxs-lookup"><span data-stu-id="7f789-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="7f789-110">Пример 2: создание операции управления API с данными запроса и ответа</span><span class="sxs-lookup"><span data-stu-id="7f789-110">Example 2: Create an API management operation with request and response details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
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
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="7f789-111">В этом примере создается операция управления API с подробными сведениями о запросе и ответе.</span><span class="sxs-lookup"><span data-stu-id="7f789-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="7f789-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f789-112">PARAMETERS</span></span>

### <span data-ttu-id="7f789-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7f789-113">-ApiId</span></span>
<span data-ttu-id="7f789-114">Задает идентификатор операции управления API.</span><span class="sxs-lookup"><span data-stu-id="7f789-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="7f789-115">-Context</span><span class="sxs-lookup"><span data-stu-id="7f789-115">-Context</span></span>
<span data-ttu-id="7f789-116">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7f789-116">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7f789-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f789-117">-DefaultProfile</span></span>
<span data-ttu-id="7f789-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f789-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="7f789-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="7f789-119">-Description</span></span>
<span data-ttu-id="7f789-120">Задает описание новой операции API.</span><span class="sxs-lookup"><span data-stu-id="7f789-120">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="7f789-121">-Method</span><span class="sxs-lookup"><span data-stu-id="7f789-121">-Method</span></span>
<span data-ttu-id="7f789-122">Задает метод HTTP для новой операции управления API.</span><span class="sxs-lookup"><span data-stu-id="7f789-122">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="7f789-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7f789-123">-Name</span></span>
<span data-ttu-id="7f789-124">Указывает отображаемое имя для новой операции управления API.</span><span class="sxs-lookup"><span data-stu-id="7f789-124">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="7f789-125">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="7f789-125">-OperationId</span></span>
<span data-ttu-id="7f789-126">Задает идентификатор операции управления API.</span><span class="sxs-lookup"><span data-stu-id="7f789-126">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="7f789-127">-Request</span><span class="sxs-lookup"><span data-stu-id="7f789-127">-Request</span></span>
<span data-ttu-id="7f789-128">Задает данные для операции управления API.</span><span class="sxs-lookup"><span data-stu-id="7f789-128">Specifies the details of the API management operation.</span></span>

```yaml
Type: PsApiManagementRequest
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f789-129">-Ответы</span><span class="sxs-lookup"><span data-stu-id="7f789-129">-Responses</span></span>
<span data-ttu-id="7f789-130">Указывает массив возможных ответов операций управления API.</span><span class="sxs-lookup"><span data-stu-id="7f789-130">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: PsApiManagementResponse[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f789-131">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="7f789-131">-TemplateParameters</span></span>
<span data-ttu-id="7f789-132">Задает массив параметров, определенных в параметре *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="7f789-132">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="7f789-133">Если этот параметр не указан, на основе *UrlTemplate* будет создано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7f789-133">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: PsApiManagementParameter[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f789-134">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="7f789-134">-UrlTemplate</span></span>
<span data-ttu-id="7f789-135">Задает шаблон URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7f789-135">Specifies the URL template.</span></span>

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

### <span data-ttu-id="7f789-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f789-136">CommonParameters</span></span>
<span data-ttu-id="7f789-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f789-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f789-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f789-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f789-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f789-139">INPUTS</span></span>

### <span data-ttu-id="7f789-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="7f789-140">None</span></span>
<span data-ttu-id="7f789-141">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7f789-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f789-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f789-142">OUTPUTS</span></span>

### <span data-ttu-id="7f789-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="7f789-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="7f789-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f789-144">NOTES</span></span>

## <span data-ttu-id="7f789-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f789-145">RELATED LINKS</span></span>

[<span data-ttu-id="7f789-146">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="7f789-146">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="7f789-147">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="7f789-147">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="7f789-148">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="7f789-148">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


