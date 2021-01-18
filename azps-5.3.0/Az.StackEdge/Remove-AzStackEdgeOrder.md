---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506403"
---
# <span data-ttu-id="1cea3-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="1cea3-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="1cea3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cea3-102">SYNOPSIS</span></span>
<span data-ttu-id="1cea3-103">Удаляет порядок устройства.</span><span class="sxs-lookup"><span data-stu-id="1cea3-103">Removes the order for a device.</span></span>

## <span data-ttu-id="1cea3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1cea3-104">SYNTAX</span></span>

### <span data-ttu-id="1cea3-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1cea3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cea3-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cea3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cea3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cea3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cea3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cea3-108">DESCRIPTION</span></span>
<span data-ttu-id="1cea3-109">С **его учетом** можно удалить существующий порядок устройств с Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="1cea3-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="1cea3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1cea3-110">EXAMPLES</span></span>

### <span data-ttu-id="1cea3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1cea3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="1cea3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cea3-112">PARAMETERS</span></span>

### <span data-ttu-id="1cea3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cea3-113">-AsJob</span></span>
<span data-ttu-id="1cea3-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1cea3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1cea3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cea3-115">-DefaultProfile</span></span>
<span data-ttu-id="1cea3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cea3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cea3-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1cea3-117">-DeviceName</span></span>
<span data-ttu-id="1cea3-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="1cea3-118">Device Name</span></span>

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

### <span data-ttu-id="1cea3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cea3-119">-InputObject</span></span>
<span data-ttu-id="1cea3-120">Объект Input</span><span class="sxs-lookup"><span data-stu-id="1cea3-120">Input Object</span></span>

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

### <span data-ttu-id="1cea3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cea3-121">-PassThru</span></span>
<span data-ttu-id="1cea3-122">возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="1cea3-122">returns true if successful</span></span>

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

### <span data-ttu-id="1cea3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cea3-123">-ResourceGroupName</span></span>
<span data-ttu-id="1cea3-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1cea3-124">Resource Group Name</span></span>

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

### <span data-ttu-id="1cea3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cea3-125">-ResourceId</span></span>
<span data-ttu-id="1cea3-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cea3-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="1cea3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cea3-127">-Confirm</span></span>
<span data-ttu-id="1cea3-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1cea3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cea3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cea3-129">-WhatIf</span></span>
<span data-ttu-id="1cea3-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cea3-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1cea3-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1cea3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cea3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cea3-132">CommonParameters</span></span>
<span data-ttu-id="1cea3-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cea3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cea3-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cea3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cea3-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1cea3-135">INPUTS</span></span>

### <span data-ttu-id="1cea3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1cea3-136">System.String</span></span>

### <span data-ttu-id="1cea3-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="1cea3-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="1cea3-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1cea3-138">OUTPUTS</span></span>

### <span data-ttu-id="1cea3-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="1cea3-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="1cea3-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1cea3-140">NOTES</span></span>

## <span data-ttu-id="1cea3-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cea3-141">RELATED LINKS</span></span>
