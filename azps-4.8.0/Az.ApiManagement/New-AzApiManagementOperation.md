---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 3cba96c2b68a3045448aa6f6f6ccd011964c6e16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077993"
---
# <span data-ttu-id="317c1-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="317c1-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="317c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="317c1-102">SYNOPSIS</span></span>
<span data-ttu-id="317c1-103">Создает операцию управления API.</span><span class="sxs-lookup"><span data-stu-id="317c1-103">Creates an API management operation.</span></span>

## <span data-ttu-id="317c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="317c1-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="317c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="317c1-105">DESCRIPTION</span></span>
<span data-ttu-id="317c1-106">Командлет **New-AzApiManagementOperation** создает операцию API.</span><span class="sxs-lookup"><span data-stu-id="317c1-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="317c1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="317c1-107">EXAMPLES</span></span>

### <span data-ttu-id="317c1-108">Пример 1: создание операции управления API</span><span class="sxs-lookup"><span data-stu-id="317c1-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="317c1-109">Эта команда создает операцию управления API.</span><span class="sxs-lookup"><span data-stu-id="317c1-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="317c1-110">Пример 2: создание операции управления API с данными запроса и ответа</span><span class="sxs-lookup"><span data-stu-id="317c1-110">Example 2: Create an API management operation with request and response details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
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
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="317c1-111">В этом примере создается операция управления API с подробными сведениями о запросе и ответе.</span><span class="sxs-lookup"><span data-stu-id="317c1-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="317c1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="317c1-112">PARAMETERS</span></span>

### <span data-ttu-id="317c1-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="317c1-113">-ApiId</span></span>
<span data-ttu-id="317c1-114">Задает идентификатор операции управления API.</span><span class="sxs-lookup"><span data-stu-id="317c1-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="317c1-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="317c1-115">-ApiRevision</span></span>
<span data-ttu-id="317c1-116">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="317c1-116">Identifier of API Revision.</span></span> <span data-ttu-id="317c1-117">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="317c1-117">This parameter is optional.</span></span> <span data-ttu-id="317c1-118">Если этот элемент не указан, операция будет присоединена к текущей активной редакции API.</span><span class="sxs-lookup"><span data-stu-id="317c1-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="317c1-119">-Context</span><span class="sxs-lookup"><span data-stu-id="317c1-119">-Context</span></span>
<span data-ttu-id="317c1-120">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="317c1-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="317c1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="317c1-121">-DefaultProfile</span></span>
<span data-ttu-id="317c1-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="317c1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="317c1-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="317c1-123">-Description</span></span>
<span data-ttu-id="317c1-124">Задает описание новой операции API.</span><span class="sxs-lookup"><span data-stu-id="317c1-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="317c1-125">-Method</span><span class="sxs-lookup"><span data-stu-id="317c1-125">-Method</span></span>
<span data-ttu-id="317c1-126">Задает метод HTTP для новой операции управления API.</span><span class="sxs-lookup"><span data-stu-id="317c1-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="317c1-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="317c1-127">-Name</span></span>
<span data-ttu-id="317c1-128">Указывает отображаемое имя для новой операции управления API.</span><span class="sxs-lookup"><span data-stu-id="317c1-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="317c1-129">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="317c1-129">-OperationId</span></span>
<span data-ttu-id="317c1-130">Задает идентификатор операции управления API.</span><span class="sxs-lookup"><span data-stu-id="317c1-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="317c1-131">-Request</span><span class="sxs-lookup"><span data-stu-id="317c1-131">-Request</span></span>
<span data-ttu-id="317c1-132">Задает данные для операции управления API.</span><span class="sxs-lookup"><span data-stu-id="317c1-132">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="317c1-133">-Ответы</span><span class="sxs-lookup"><span data-stu-id="317c1-133">-Responses</span></span>
<span data-ttu-id="317c1-134">Указывает массив возможных ответов операций управления API.</span><span class="sxs-lookup"><span data-stu-id="317c1-134">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="317c1-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="317c1-135">-TemplateParameters</span></span>
<span data-ttu-id="317c1-136">Задает массив параметров, определенных в параметре *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="317c1-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="317c1-137">Если этот параметр не указан, на основе *UrlTemplate* будет создано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="317c1-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="317c1-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="317c1-138">-UrlTemplate</span></span>
<span data-ttu-id="317c1-139">Задает шаблон URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="317c1-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="317c1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="317c1-140">CommonParameters</span></span>
<span data-ttu-id="317c1-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="317c1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="317c1-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="317c1-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="317c1-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="317c1-143">INPUTS</span></span>

### <span data-ttu-id="317c1-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="317c1-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="317c1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="317c1-145">System.String</span></span>

### <span data-ttu-id="317c1-146">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="317c1-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="317c1-147">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="317c1-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="317c1-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="317c1-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="317c1-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="317c1-149">OUTPUTS</span></span>

### <span data-ttu-id="317c1-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="317c1-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="317c1-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="317c1-151">NOTES</span></span>

## <span data-ttu-id="317c1-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="317c1-152">RELATED LINKS</span></span>

[<span data-ttu-id="317c1-153">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="317c1-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="317c1-154">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="317c1-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="317c1-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="317c1-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


