---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249781"
---
# <span data-ttu-id="a3863-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a3863-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="a3863-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3863-102">SYNOPSIS</span></span>
<span data-ttu-id="a3863-103">Удаление расписания пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="a3863-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="a3863-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3863-104">SYNTAX</span></span>

### <span data-ttu-id="a3863-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3863-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3863-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3863-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3863-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3863-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3863-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3863-108">DESCRIPTION</span></span>
<span data-ttu-id="a3863-109">Командлет **Remove-AzStackEdgeBandwidthSchedule** Удаляет расписание пропускной способности для краевого устройства стека.</span><span class="sxs-lookup"><span data-stu-id="a3863-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="a3863-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3863-110">EXAMPLES</span></span>

### <span data-ttu-id="a3863-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a3863-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="a3863-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3863-112">PARAMETERS</span></span>

### <span data-ttu-id="a3863-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3863-113">-AsJob</span></span>
<span data-ttu-id="a3863-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a3863-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3863-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3863-115">-DefaultProfile</span></span>
<span data-ttu-id="a3863-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3863-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3863-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="a3863-117">-DeviceName</span></span>
<span data-ttu-id="a3863-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="a3863-118">Device Name</span></span>

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

### <span data-ttu-id="a3863-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3863-119">-InputObject</span></span>
<span data-ttu-id="a3863-120">Объект input</span><span class="sxs-lookup"><span data-stu-id="a3863-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3863-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a3863-121">-Name</span></span>
<span data-ttu-id="a3863-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="a3863-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3863-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3863-123">-PassThru</span></span>
<span data-ttu-id="a3863-124">Возвращает значение истина, если выполнено успешно</span><span class="sxs-lookup"><span data-stu-id="a3863-124">returns true if successful</span></span>

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

### <span data-ttu-id="a3863-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3863-125">-ResourceGroupName</span></span>
<span data-ttu-id="a3863-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a3863-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a3863-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3863-127">-ResourceId</span></span>
<span data-ttu-id="a3863-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3863-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="a3863-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3863-129">-Confirm</span></span>
<span data-ttu-id="a3863-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a3863-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3863-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3863-131">-WhatIf</span></span>
<span data-ttu-id="a3863-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a3863-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3863-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a3863-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3863-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3863-134">CommonParameters</span></span>
<span data-ttu-id="a3863-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3863-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3863-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3863-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3863-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3863-137">INPUTS</span></span>

### <span data-ttu-id="a3863-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a3863-138">System.String</span></span>

### <span data-ttu-id="a3863-139">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a3863-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="a3863-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3863-140">OUTPUTS</span></span>

### <span data-ttu-id="a3863-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3863-141">System.Boolean</span></span>

## <span data-ttu-id="a3863-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3863-142">NOTES</span></span>

## <span data-ttu-id="a3863-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3863-143">RELATED LINKS</span></span>
