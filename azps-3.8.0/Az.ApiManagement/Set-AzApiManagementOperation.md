---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
ms.openlocfilehash: 92848cb2daa0976d8206549fc16d1a6f039199a6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074178"
---
# <span data-ttu-id="588c3-101">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="588c3-101">Set-AzApiManagementOperation</span></span>

## <span data-ttu-id="588c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="588c3-102">SYNOPSIS</span></span>
<span data-ttu-id="588c3-103">Задает сведения об операции API.</span><span class="sxs-lookup"><span data-stu-id="588c3-103">Sets API operation details.</span></span>

## <span data-ttu-id="588c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="588c3-104">SYNTAX</span></span>

```
Set-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="588c3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="588c3-105">DESCRIPTION</span></span>
<span data-ttu-id="588c3-106">Командлет **Set-AzApiManagementOperation** задает сведения об операциях API.</span><span class="sxs-lookup"><span data-stu-id="588c3-106">The **Set-AzApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="588c3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="588c3-107">EXAMPLES</span></span>

### <span data-ttu-id="588c3-108">Пример 1: Настройка сведений об операции</span><span class="sxs-lookup"><span data-stu-id="588c3-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="588c3-109">Эта команда задает сведения об операциях для управления API.</span><span class="sxs-lookup"><span data-stu-id="588c3-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="588c3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="588c3-110">PARAMETERS</span></span>

### <span data-ttu-id="588c3-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="588c3-111">-ApiId</span></span>
<span data-ttu-id="588c3-112">Указывает идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="588c3-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="588c3-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="588c3-113">-ApiRevision</span></span>
<span data-ttu-id="588c3-114">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="588c3-114">Identifier of API Revision.</span></span> <span data-ttu-id="588c3-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="588c3-115">This parameter is optional.</span></span> <span data-ttu-id="588c3-116">Если этот элемент не указан, операция будет обновлена в текущей активной редакции API.</span><span class="sxs-lookup"><span data-stu-id="588c3-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="588c3-117">-Context</span><span class="sxs-lookup"><span data-stu-id="588c3-117">-Context</span></span>
<span data-ttu-id="588c3-118">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="588c3-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="588c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="588c3-119">-DefaultProfile</span></span>
<span data-ttu-id="588c3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="588c3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="588c3-121">-Описание</span><span class="sxs-lookup"><span data-stu-id="588c3-121">-Description</span></span>
<span data-ttu-id="588c3-122">Задает описание новой операции.</span><span class="sxs-lookup"><span data-stu-id="588c3-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="588c3-123">-Method</span><span class="sxs-lookup"><span data-stu-id="588c3-123">-Method</span></span>
<span data-ttu-id="588c3-124">Задает метод HTTP для новой операции.</span><span class="sxs-lookup"><span data-stu-id="588c3-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="588c3-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="588c3-125">-Name</span></span>
<span data-ttu-id="588c3-126">Указывает отображаемое имя для новой операции.</span><span class="sxs-lookup"><span data-stu-id="588c3-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="588c3-127">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="588c3-127">-OperationId</span></span>
<span data-ttu-id="588c3-128">Указывает идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="588c3-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="588c3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="588c3-129">-PassThru</span></span>
<span data-ttu-id="588c3-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="588c3-130">passthru</span></span>

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

### <span data-ttu-id="588c3-131">-Request</span><span class="sxs-lookup"><span data-stu-id="588c3-131">-Request</span></span>
<span data-ttu-id="588c3-132">Задает сведения о запросе операции.</span><span class="sxs-lookup"><span data-stu-id="588c3-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="588c3-133">-Ответы</span><span class="sxs-lookup"><span data-stu-id="588c3-133">-Responses</span></span>
<span data-ttu-id="588c3-134">Указывает массив возможных ответов операций.</span><span class="sxs-lookup"><span data-stu-id="588c3-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="588c3-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="588c3-135">-TemplateParameters</span></span>
<span data-ttu-id="588c3-136">Задает массив или параметры, определенные в параметре *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="588c3-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="588c3-137">Если значение не задано, на основе UrlTemplate будет создано значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="588c3-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="588c3-138">С помощью этого параметра можно получить дополнительные сведения о таких параметрах, как описание, тип и другие возможные значения.</span><span class="sxs-lookup"><span data-stu-id="588c3-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="588c3-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="588c3-139">-UrlTemplate</span></span>
<span data-ttu-id="588c3-140">Задает шаблон URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="588c3-140">Specifies the URL template.</span></span>
<span data-ttu-id="588c3-141">Например: Customers/{CID}/заказы/{OID}/? Дата = {Date}.</span><span class="sxs-lookup"><span data-stu-id="588c3-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="588c3-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="588c3-142">-Confirm</span></span>
<span data-ttu-id="588c3-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="588c3-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="588c3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="588c3-144">-WhatIf</span></span>
<span data-ttu-id="588c3-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="588c3-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="588c3-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="588c3-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="588c3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="588c3-147">CommonParameters</span></span>
<span data-ttu-id="588c3-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="588c3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="588c3-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="588c3-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="588c3-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="588c3-150">INPUTS</span></span>

### <span data-ttu-id="588c3-151">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="588c3-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="588c3-152">System. String</span><span class="sxs-lookup"><span data-stu-id="588c3-152">System.String</span></span>

### <span data-ttu-id="588c3-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="588c3-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="588c3-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="588c3-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="588c3-155">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="588c3-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="588c3-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="588c3-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="588c3-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="588c3-157">OUTPUTS</span></span>

### <span data-ttu-id="588c3-158">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="588c3-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="588c3-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="588c3-159">NOTES</span></span>

## <span data-ttu-id="588c3-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="588c3-160">RELATED LINKS</span></span>

[<span data-ttu-id="588c3-161">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="588c3-161">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="588c3-162">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="588c3-162">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="588c3-163">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="588c3-163">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)


