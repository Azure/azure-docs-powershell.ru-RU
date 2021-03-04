---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 44eb7ef52782f6a00a81385f7b1a87b0292bec33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959859"
---
# <span data-ttu-id="76cc9-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="76cc9-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="76cc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="76cc9-103">Создает операцию управления API.</span><span class="sxs-lookup"><span data-stu-id="76cc9-103">Creates an API management operation.</span></span>

## <span data-ttu-id="76cc9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76cc9-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76cc9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76cc9-105">DESCRIPTION</span></span>
<span data-ttu-id="76cc9-106">Для создания API создается операция **New-AzApiManagementOperation.**</span><span class="sxs-lookup"><span data-stu-id="76cc9-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="76cc9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76cc9-107">EXAMPLES</span></span>

### <span data-ttu-id="76cc9-108">Пример 1. Создание операции управления API</span><span class="sxs-lookup"><span data-stu-id="76cc9-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="76cc9-109">Эта команда создает операцию управления API.</span><span class="sxs-lookup"><span data-stu-id="76cc9-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="76cc9-110">Пример 2. Создание операции управления API со сведениями о запросах и ответах</span><span class="sxs-lookup"><span data-stu-id="76cc9-110">Example 2: Create an API management operation with request and response details</span></span>
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

<span data-ttu-id="76cc9-111">В этом примере создается операция управления API со сведениями о запросах и ответах.</span><span class="sxs-lookup"><span data-stu-id="76cc9-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="76cc9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76cc9-112">PARAMETERS</span></span>

### <span data-ttu-id="76cc9-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="76cc9-113">-ApiId</span></span>
<span data-ttu-id="76cc9-114">Определяет идентификатор операции управления API.</span><span class="sxs-lookup"><span data-stu-id="76cc9-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="76cc9-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="76cc9-115">-ApiRevision</span></span>
<span data-ttu-id="76cc9-116">Идентификатор изменения API.</span><span class="sxs-lookup"><span data-stu-id="76cc9-116">Identifier of API Revision.</span></span> <span data-ttu-id="76cc9-117">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="76cc9-117">This parameter is optional.</span></span> <span data-ttu-id="76cc9-118">Если не указано, операция будет привязана к активной редакции API.</span><span class="sxs-lookup"><span data-stu-id="76cc9-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="76cc9-119">-Контекст</span><span class="sxs-lookup"><span data-stu-id="76cc9-119">-Context</span></span>
<span data-ttu-id="76cc9-120">Указывает экземпляр объекта **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="76cc9-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="76cc9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76cc9-121">-DefaultProfile</span></span>
<span data-ttu-id="76cc9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76cc9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76cc9-123">-Description</span><span class="sxs-lookup"><span data-stu-id="76cc9-123">-Description</span></span>
<span data-ttu-id="76cc9-124">Описание новой операции API.</span><span class="sxs-lookup"><span data-stu-id="76cc9-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="76cc9-125">-Method</span><span class="sxs-lookup"><span data-stu-id="76cc9-125">-Method</span></span>
<span data-ttu-id="76cc9-126">Метод HTTP для новой операции управления API.</span><span class="sxs-lookup"><span data-stu-id="76cc9-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="76cc9-127">-Name</span><span class="sxs-lookup"><span data-stu-id="76cc9-127">-Name</span></span>
<span data-ttu-id="76cc9-128">Отображает имя новой операции управления API.</span><span class="sxs-lookup"><span data-stu-id="76cc9-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="76cc9-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="76cc9-129">-OperationId</span></span>
<span data-ttu-id="76cc9-130">Определяет идентификатор операции управления API.</span><span class="sxs-lookup"><span data-stu-id="76cc9-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="76cc9-131">-Request</span><span class="sxs-lookup"><span data-stu-id="76cc9-131">-Request</span></span>
<span data-ttu-id="76cc9-132">Подробные сведения об управлении API.</span><span class="sxs-lookup"><span data-stu-id="76cc9-132">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="76cc9-133">-Ответы</span><span class="sxs-lookup"><span data-stu-id="76cc9-133">-Responses</span></span>
<span data-ttu-id="76cc9-134">Определяет массив возможных ответов на операции управления API.</span><span class="sxs-lookup"><span data-stu-id="76cc9-134">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="76cc9-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="76cc9-135">-TemplateParameters</span></span>
<span data-ttu-id="76cc9-136">Указывает массив параметров, определенный в *параметре URLTemplate.*</span><span class="sxs-lookup"><span data-stu-id="76cc9-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="76cc9-137">Если этот параметр не указан, будет сгенерировано значение по умолчанию на основе *URLTemplate.*</span><span class="sxs-lookup"><span data-stu-id="76cc9-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="76cc9-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="76cc9-138">-UrlTemplate</span></span>
<span data-ttu-id="76cc9-139">Определяет шаблон URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="76cc9-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="76cc9-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76cc9-140">CommonParameters</span></span>
<span data-ttu-id="76cc9-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76cc9-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76cc9-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76cc9-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76cc9-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76cc9-143">INPUTS</span></span>

### <span data-ttu-id="76cc9-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="76cc9-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="76cc9-145">System.String</span><span class="sxs-lookup"><span data-stu-id="76cc9-145">System.String</span></span>

### <span data-ttu-id="76cc9-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span><span class="sxs-lookup"><span data-stu-id="76cc9-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="76cc9-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="76cc9-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="76cc9-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span><span class="sxs-lookup"><span data-stu-id="76cc9-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="76cc9-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76cc9-149">OUTPUTS</span></span>

### <span data-ttu-id="76cc9-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="76cc9-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="76cc9-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76cc9-151">NOTES</span></span>

## <span data-ttu-id="76cc9-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76cc9-152">RELATED LINKS</span></span>

[<span data-ttu-id="76cc9-153">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="76cc9-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="76cc9-154">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="76cc9-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="76cc9-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="76cc9-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


