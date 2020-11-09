---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: 153eb354ae8ba0f033a34010658b0d851572ddd6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319370"
---
# <span data-ttu-id="86836-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="86836-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="86836-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86836-102">SYNOPSIS</span></span>
<span data-ttu-id="86836-103">Удаляет существующую операцию.</span><span class="sxs-lookup"><span data-stu-id="86836-103">Removes an existing operation.</span></span>

## <span data-ttu-id="86836-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86836-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86836-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86836-105">DESCRIPTION</span></span>
<span data-ttu-id="86836-106">Командлет **Remove-AzApiManagementOperation** удаляет существующую операцию.</span><span class="sxs-lookup"><span data-stu-id="86836-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="86836-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86836-107">EXAMPLES</span></span>

### <span data-ttu-id="86836-108">Пример 1: удаление существующей операции API</span><span class="sxs-lookup"><span data-stu-id="86836-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="86836-109">Эта команда удаляет существующую операцию API.</span><span class="sxs-lookup"><span data-stu-id="86836-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="86836-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86836-110">PARAMETERS</span></span>

### <span data-ttu-id="86836-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="86836-111">-ApiId</span></span>
<span data-ttu-id="86836-112">Указывает идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="86836-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="86836-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="86836-113">-ApiRevision</span></span>
<span data-ttu-id="86836-114">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="86836-114">Identifier of API Revision.</span></span> <span data-ttu-id="86836-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="86836-115">This parameter is optional.</span></span> <span data-ttu-id="86836-116">Если не указано, операция будет удалена из текущей активной версии API.</span><span class="sxs-lookup"><span data-stu-id="86836-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="86836-117">-Context</span><span class="sxs-lookup"><span data-stu-id="86836-117">-Context</span></span>
<span data-ttu-id="86836-118">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="86836-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="86836-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86836-119">-DefaultProfile</span></span>
<span data-ttu-id="86836-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86836-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86836-121">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="86836-121">-OperationId</span></span>
<span data-ttu-id="86836-122">Задает идентификатор операции API.</span><span class="sxs-lookup"><span data-stu-id="86836-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="86836-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86836-123">-PassThru</span></span>
<span data-ttu-id="86836-124">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="86836-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="86836-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86836-125">-Confirm</span></span>
<span data-ttu-id="86836-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="86836-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86836-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86836-127">-WhatIf</span></span>
<span data-ttu-id="86836-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="86836-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86836-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="86836-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86836-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86836-130">CommonParameters</span></span>
<span data-ttu-id="86836-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86836-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86836-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86836-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86836-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86836-133">INPUTS</span></span>

### <span data-ttu-id="86836-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="86836-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="86836-135">System. String</span><span class="sxs-lookup"><span data-stu-id="86836-135">System.String</span></span>

### <span data-ttu-id="86836-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="86836-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="86836-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86836-137">OUTPUTS</span></span>

### <span data-ttu-id="86836-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86836-138">System.Boolean</span></span>

## <span data-ttu-id="86836-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="86836-139">NOTES</span></span>

## <span data-ttu-id="86836-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86836-140">RELATED LINKS</span></span>

[<span data-ttu-id="86836-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="86836-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="86836-142">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="86836-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="86836-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="86836-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


