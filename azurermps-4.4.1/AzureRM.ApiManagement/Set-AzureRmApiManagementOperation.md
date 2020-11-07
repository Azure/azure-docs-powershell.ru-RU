---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 28bbc9158639faf066fa9a623f5dfacd6566d236
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734276"
---
# <span data-ttu-id="f3f75-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f3f75-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="f3f75-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3f75-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f75-103">Задает сведения об операции API.</span><span class="sxs-lookup"><span data-stu-id="f3f75-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3f75-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3f75-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3f75-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3f75-105">DESCRIPTION</span></span>
<span data-ttu-id="f3f75-106">Командлет **Set-AzureRmApiManagementOperation** задает сведения об операциях API.</span><span class="sxs-lookup"><span data-stu-id="f3f75-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="f3f75-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3f75-107">EXAMPLES</span></span>

### <span data-ttu-id="f3f75-108">Пример 1: Настройка сведений об операции</span><span class="sxs-lookup"><span data-stu-id="f3f75-108">Example 1: Set the operation details</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="f3f75-109">Эта команда задает сведения об операциях для управления API.</span><span class="sxs-lookup"><span data-stu-id="f3f75-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="f3f75-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3f75-110">PARAMETERS</span></span>

### <span data-ttu-id="f3f75-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f3f75-111">-ApiId</span></span>
<span data-ttu-id="f3f75-112">Указывает идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="f3f75-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="f3f75-113">-Context</span><span class="sxs-lookup"><span data-stu-id="f3f75-113">-Context</span></span>
<span data-ttu-id="f3f75-114">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="f3f75-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="f3f75-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="f3f75-115">-Description</span></span>
<span data-ttu-id="f3f75-116">Задает описание новой операции.</span><span class="sxs-lookup"><span data-stu-id="f3f75-116">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="f3f75-117">-Method</span><span class="sxs-lookup"><span data-stu-id="f3f75-117">-Method</span></span>
<span data-ttu-id="f3f75-118">Задает метод HTTP для новой операции.</span><span class="sxs-lookup"><span data-stu-id="f3f75-118">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="f3f75-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f3f75-119">-Name</span></span>
<span data-ttu-id="f3f75-120">Указывает отображаемое имя для новой операции.</span><span class="sxs-lookup"><span data-stu-id="f3f75-120">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="f3f75-121">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="f3f75-121">-OperationId</span></span>
<span data-ttu-id="f3f75-122">Указывает идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="f3f75-122">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="f3f75-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3f75-123">-PassThru</span></span>
<span data-ttu-id="f3f75-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="f3f75-124">passthru</span></span>

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

### <span data-ttu-id="f3f75-125">-Request</span><span class="sxs-lookup"><span data-stu-id="f3f75-125">-Request</span></span>
<span data-ttu-id="f3f75-126">Задает сведения о запросе операции.</span><span class="sxs-lookup"><span data-stu-id="f3f75-126">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="f3f75-127">-Ответы</span><span class="sxs-lookup"><span data-stu-id="f3f75-127">-Responses</span></span>
<span data-ttu-id="f3f75-128">Указывает массив возможных ответов операций.</span><span class="sxs-lookup"><span data-stu-id="f3f75-128">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="f3f75-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="f3f75-129">-TemplateParameters</span></span>
<span data-ttu-id="f3f75-130">Задает массив или параметры, определенные в параметре *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="f3f75-130">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="f3f75-131">Если значение не задано, на основе UrlTemplate будет создано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3f75-131">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="f3f75-132">С помощью этого параметра можно получить дополнительные сведения о таких параметрах, как описание, тип и другие возможные значения.</span><span class="sxs-lookup"><span data-stu-id="f3f75-132">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="f3f75-133">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="f3f75-133">-UrlTemplate</span></span>
<span data-ttu-id="f3f75-134">Задает шаблон URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="f3f75-134">Specifies the URL template.</span></span>
<span data-ttu-id="f3f75-135">Например: Customers/{CID}/заказы/{OID}/? Дата = {Date}.</span><span class="sxs-lookup"><span data-stu-id="f3f75-135">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="f3f75-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f75-136">-DefaultProfile</span></span>
<span data-ttu-id="f3f75-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3f75-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3f75-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f75-138">CommonParameters</span></span>
<span data-ttu-id="f3f75-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3f75-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f75-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3f75-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f75-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3f75-141">INPUTS</span></span>

## <span data-ttu-id="f3f75-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3f75-142">OUTPUTS</span></span>

### <span data-ttu-id="f3f75-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f3f75-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="f3f75-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3f75-144">NOTES</span></span>

## <span data-ttu-id="f3f75-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3f75-145">RELATED LINKS</span></span>

[<span data-ttu-id="f3f75-146">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f3f75-146">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f3f75-147">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f3f75-147">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f3f75-148">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f3f75-148">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


