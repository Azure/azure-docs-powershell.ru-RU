---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
ms.openlocfilehash: b3a99d286c0efcf76dee0c71d8d3b5f4e704ca40
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508593"
---
# <span data-ttu-id="da26f-101">Remove-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="da26f-101">Remove-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="da26f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da26f-102">SYNOPSIS</span></span>
<span data-ttu-id="da26f-103">Удаляет связанную роль IoT для устройства.</span><span class="sxs-lookup"><span data-stu-id="da26f-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="da26f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da26f-104">SYNTAX</span></span>

### <span data-ttu-id="da26f-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da26f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da26f-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da26f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da26f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da26f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -InputObject <PSDataBoxEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da26f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da26f-108">DESCRIPTION</span></span>
<span data-ttu-id="da26f-109">Для **устройства Edge Data Box** удаляется связанная с ней роль IoT.</span><span class="sxs-lookup"><span data-stu-id="da26f-109">The **Remove-AzDataBoxEdgeRole** cmdlet removes the associated IoT role for a Data Box Edge device.</span></span>

## <span data-ttu-id="da26f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da26f-110">EXAMPLES</span></span>

### <span data-ttu-id="da26f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="da26f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="da26f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da26f-112">PARAMETERS</span></span>

### <span data-ttu-id="da26f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da26f-113">-AsJob</span></span>
<span data-ttu-id="da26f-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="da26f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da26f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da26f-115">-DefaultProfile</span></span>
<span data-ttu-id="da26f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da26f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da26f-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="da26f-117">-DeviceName</span></span>
<span data-ttu-id="da26f-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="da26f-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da26f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da26f-119">-InputObject</span></span>
<span data-ttu-id="da26f-120">Объект Input</span><span class="sxs-lookup"><span data-stu-id="da26f-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da26f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="da26f-121">-Name</span></span>
<span data-ttu-id="da26f-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="da26f-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da26f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da26f-123">-PassThru</span></span>
<span data-ttu-id="da26f-124">Возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="da26f-124">returns true if successful</span></span>

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

### <span data-ttu-id="da26f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da26f-125">-ResourceGroupName</span></span>
<span data-ttu-id="da26f-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="da26f-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da26f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da26f-127">-ResourceId</span></span>
<span data-ttu-id="da26f-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="da26f-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="da26f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da26f-129">-Confirm</span></span>
<span data-ttu-id="da26f-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="da26f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da26f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da26f-131">-WhatIf</span></span>
<span data-ttu-id="da26f-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da26f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da26f-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="da26f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da26f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da26f-134">CommonParameters</span></span>
<span data-ttu-id="da26f-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da26f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da26f-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da26f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da26f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da26f-137">INPUTS</span></span>

### <span data-ttu-id="da26f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="da26f-138">System.String</span></span>

### <span data-ttu-id="da26f-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="da26f-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="da26f-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da26f-140">OUTPUTS</span></span>

### <span data-ttu-id="da26f-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="da26f-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="da26f-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da26f-142">NOTES</span></span>

## <span data-ttu-id="da26f-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da26f-143">RELATED LINKS</span></span>
