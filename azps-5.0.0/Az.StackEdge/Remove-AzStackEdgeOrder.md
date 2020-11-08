---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246513"
---
# <span data-ttu-id="e8045-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="e8045-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="e8045-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8045-102">SYNOPSIS</span></span>
<span data-ttu-id="e8045-103">Удаление порядка устройства.</span><span class="sxs-lookup"><span data-stu-id="e8045-103">Removes the order for a device.</span></span>

## <span data-ttu-id="e8045-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8045-104">SYNTAX</span></span>

### <span data-ttu-id="e8045-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8045-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8045-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8045-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8045-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8045-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8045-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8045-108">DESCRIPTION</span></span>
<span data-ttu-id="e8045-109">Командлет **Remove-AzStackEdgeOrder** удаляет существующий заказ для краевого устройства стека.</span><span class="sxs-lookup"><span data-stu-id="e8045-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="e8045-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8045-110">EXAMPLES</span></span>

### <span data-ttu-id="e8045-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8045-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="e8045-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8045-112">PARAMETERS</span></span>

### <span data-ttu-id="e8045-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8045-113">-AsJob</span></span>
<span data-ttu-id="e8045-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e8045-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8045-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8045-115">-DefaultProfile</span></span>
<span data-ttu-id="e8045-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8045-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8045-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="e8045-117">-DeviceName</span></span>
<span data-ttu-id="e8045-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="e8045-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8045-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8045-119">-InputObject</span></span>
<span data-ttu-id="e8045-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="e8045-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8045-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8045-121">-PassThru</span></span>
<span data-ttu-id="e8045-122">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="e8045-122">returns true if successful</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8045-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8045-123">-ResourceGroupName</span></span>
<span data-ttu-id="e8045-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e8045-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8045-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8045-125">-ResourceId</span></span>
<span data-ttu-id="e8045-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8045-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8045-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8045-127">-Confirm</span></span>
<span data-ttu-id="e8045-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8045-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8045-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8045-129">-WhatIf</span></span>
<span data-ttu-id="e8045-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8045-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8045-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8045-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8045-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8045-132">CommonParameters</span></span>
<span data-ttu-id="e8045-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8045-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8045-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8045-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8045-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8045-135">INPUTS</span></span>

### <span data-ttu-id="e8045-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e8045-136">System.String</span></span>

### <span data-ttu-id="e8045-137">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="e8045-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="e8045-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8045-138">OUTPUTS</span></span>

### <span data-ttu-id="e8045-139">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="e8045-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="e8045-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8045-140">NOTES</span></span>

## <span data-ttu-id="e8045-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8045-141">RELATED LINKS</span></span>
