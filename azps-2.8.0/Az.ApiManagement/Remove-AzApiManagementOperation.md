---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4A8D996-72A2-4154-98DA-5F84CAA010B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOperation.md
ms.openlocfilehash: b5d52c4fa70312e276851cb3043c7dbd7babdc1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727980"
---
# <span data-ttu-id="d6069-101">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6069-101">Remove-AzApiManagementOperation</span></span>

## <span data-ttu-id="d6069-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6069-102">SYNOPSIS</span></span>
<span data-ttu-id="d6069-103">Удаляет существующую операцию.</span><span class="sxs-lookup"><span data-stu-id="d6069-103">Removes an existing operation.</span></span>

## <span data-ttu-id="d6069-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6069-104">SYNTAX</span></span>

```
Remove-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6069-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6069-105">DESCRIPTION</span></span>
<span data-ttu-id="d6069-106">Командлет **Remove-AzApiManagementOperation** удаляет существующую операцию.</span><span class="sxs-lookup"><span data-stu-id="d6069-106">The **Remove-AzApiManagementOperation** cmdlet removes an existing operation.</span></span>

## <span data-ttu-id="d6069-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6069-107">EXAMPLES</span></span>

### <span data-ttu-id="d6069-108">Пример 1: удаление существующей операции API</span><span class="sxs-lookup"><span data-stu-id="d6069-108">Example 1: Remove an existing API Operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOperation -Context $apimContext -ApiId "0123456789" -OperationId "9876543210" -Force
```

<span data-ttu-id="d6069-109">Эта команда удаляет существующую операцию API.</span><span class="sxs-lookup"><span data-stu-id="d6069-109">This command removes an existing API Operation.</span></span>

## <span data-ttu-id="d6069-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6069-110">PARAMETERS</span></span>

### <span data-ttu-id="d6069-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d6069-111">-ApiId</span></span>
<span data-ttu-id="d6069-112">Указывает идентификатор API.</span><span class="sxs-lookup"><span data-stu-id="d6069-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="d6069-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d6069-113">-ApiRevision</span></span>
<span data-ttu-id="d6069-114">Идентификатор редакции API.</span><span class="sxs-lookup"><span data-stu-id="d6069-114">Identifier of API Revision.</span></span> <span data-ttu-id="d6069-115">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="d6069-115">This parameter is optional.</span></span> <span data-ttu-id="d6069-116">Если не указано, операция будет удалена из текущей активной версии API.</span><span class="sxs-lookup"><span data-stu-id="d6069-116">If not specified, the operation will be removed from the currently active api revision.</span></span>

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

### <span data-ttu-id="d6069-117">-Context</span><span class="sxs-lookup"><span data-stu-id="d6069-117">-Context</span></span>
<span data-ttu-id="d6069-118">Указывает экземпляр **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="d6069-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="d6069-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6069-119">-DefaultProfile</span></span>
<span data-ttu-id="d6069-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6069-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6069-121">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="d6069-121">-OperationId</span></span>
<span data-ttu-id="d6069-122">Задает идентификатор операции API.</span><span class="sxs-lookup"><span data-stu-id="d6069-122">Specifies the identifier of the API operation.</span></span>

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

### <span data-ttu-id="d6069-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6069-123">-PassThru</span></span>
<span data-ttu-id="d6069-124">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или значение $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d6069-124">Indicates that this cmdlet returns a value of $True if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="d6069-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6069-125">-Confirm</span></span>
<span data-ttu-id="d6069-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d6069-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6069-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6069-127">-WhatIf</span></span>
<span data-ttu-id="d6069-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d6069-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6069-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d6069-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6069-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6069-130">CommonParameters</span></span>
<span data-ttu-id="d6069-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6069-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6069-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6069-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6069-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6069-133">INPUTS</span></span>

### <span data-ttu-id="d6069-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d6069-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d6069-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d6069-135">System.String</span></span>

### <span data-ttu-id="d6069-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d6069-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d6069-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6069-137">OUTPUTS</span></span>

### <span data-ttu-id="d6069-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d6069-138">System.Boolean</span></span>

## <span data-ttu-id="d6069-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6069-139">NOTES</span></span>

## <span data-ttu-id="d6069-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6069-140">RELATED LINKS</span></span>

[<span data-ttu-id="d6069-141">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6069-141">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="d6069-142">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6069-142">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="d6069-143">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="d6069-143">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


