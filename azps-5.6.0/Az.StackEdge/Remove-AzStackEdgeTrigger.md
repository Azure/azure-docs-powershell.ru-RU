---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: e7659c6437e9566a4793e12518a30067aa73297a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005075"
---
# <span data-ttu-id="43cdf-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="43cdf-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="43cdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43cdf-102">SYNOPSIS</span></span>
<span data-ttu-id="43cdf-103">Удаляет существующий триггер на устройстве.</span><span class="sxs-lookup"><span data-stu-id="43cdf-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="43cdf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="43cdf-104">SYNTAX</span></span>

### <span data-ttu-id="43cdf-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43cdf-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43cdf-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43cdf-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43cdf-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43cdf-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43cdf-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43cdf-108">DESCRIPTION</span></span>
<span data-ttu-id="43cdf-109">Для удаления существующего триггера на устройстве Stack Edge удаляется существующий триггер **Remove-AzStackEdgeTrigger.**</span><span class="sxs-lookup"><span data-stu-id="43cdf-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="43cdf-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="43cdf-110">EXAMPLES</span></span>

### <span data-ttu-id="43cdf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43cdf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="43cdf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43cdf-112">PARAMETERS</span></span>

### <span data-ttu-id="43cdf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43cdf-113">-AsJob</span></span>
<span data-ttu-id="43cdf-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="43cdf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43cdf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43cdf-115">-DefaultProfile</span></span>
<span data-ttu-id="43cdf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43cdf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43cdf-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="43cdf-117">-DeviceName</span></span>
<span data-ttu-id="43cdf-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="43cdf-118">Device Name</span></span>

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

### <span data-ttu-id="43cdf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43cdf-119">-InputObject</span></span>
<span data-ttu-id="43cdf-120">Объект Input</span><span class="sxs-lookup"><span data-stu-id="43cdf-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Trigger

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43cdf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="43cdf-121">-Name</span></span>
<span data-ttu-id="43cdf-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="43cdf-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43cdf-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43cdf-123">-PassThru</span></span>
<span data-ttu-id="43cdf-124">Возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="43cdf-124">returns true if successful</span></span>

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

### <span data-ttu-id="43cdf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43cdf-125">-ResourceGroupName</span></span>
<span data-ttu-id="43cdf-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="43cdf-126">Resource Group Name</span></span>

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

### <span data-ttu-id="43cdf-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43cdf-127">-ResourceId</span></span>
<span data-ttu-id="43cdf-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="43cdf-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43cdf-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43cdf-129">-Confirm</span></span>
<span data-ttu-id="43cdf-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="43cdf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43cdf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43cdf-131">-WhatIf</span></span>
<span data-ttu-id="43cdf-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43cdf-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43cdf-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="43cdf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43cdf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43cdf-134">CommonParameters</span></span>
<span data-ttu-id="43cdf-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43cdf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43cdf-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43cdf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43cdf-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43cdf-137">INPUTS</span></span>

### <span data-ttu-id="43cdf-138">System.String</span><span class="sxs-lookup"><span data-stu-id="43cdf-138">System.String</span></span>

### <span data-ttu-id="43cdf-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="43cdf-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="43cdf-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43cdf-140">OUTPUTS</span></span>

### <span data-ttu-id="43cdf-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="43cdf-141">System.Boolean</span></span>

## <span data-ttu-id="43cdf-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="43cdf-142">NOTES</span></span>

## <span data-ttu-id="43cdf-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43cdf-143">RELATED LINKS</span></span>
