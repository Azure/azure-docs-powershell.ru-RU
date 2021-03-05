---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 17221e2d4f88e2f59ee13f73fb18132c01f6632e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994888"
---
# <span data-ttu-id="7d3b4-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="7d3b4-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="7d3b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d3b4-102">SYNOPSIS</span></span>
<span data-ttu-id="7d3b4-103">Обновляет расписание пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="7d3b4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7d3b4-104">SYNTAX</span></span>

### <span data-ttu-id="7d3b4-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d3b4-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3b4-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d3b4-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d3b4-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="7d3b4-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3b4-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="7d3b4-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3b4-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d3b4-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3b4-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="7d3b4-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3b4-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="7d3b4-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3b4-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="7d3b4-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3b4-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="7d3b4-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d3b4-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d3b4-114">DESCRIPTION</span></span>
<span data-ttu-id="7d3b4-115">**Cmdlet Set-AzStackEdgeBandwidthSchedule** обновляет расписание пропускной способности для устройства Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="7d3b4-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7d3b4-116">EXAMPLES</span></span>

### <span data-ttu-id="7d3b4-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7d3b4-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="7d3b4-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7d3b4-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="7d3b4-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d3b4-119">PARAMETERS</span></span>

### <span data-ttu-id="7d3b4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d3b4-120">-AsJob</span></span>
<span data-ttu-id="7d3b4-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7d3b4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d3b4-122">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="7d3b4-122">-Bandwidth</span></span>
<span data-ttu-id="7d3b4-123">Пропускная способность в Мбит/с</span><span class="sxs-lookup"><span data-stu-id="7d3b4-123">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateByResourceIdParameterBandwidthSet, UpdateByInputObjectParameterBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3b4-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="7d3b4-124">-DaysOfWeek</span></span>
<span data-ttu-id="7d3b4-125">Запланированные дниOfWeek</span><span class="sxs-lookup"><span data-stu-id="7d3b4-125">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3b4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d3b4-126">-DefaultProfile</span></span>
<span data-ttu-id="7d3b4-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d3b4-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7d3b4-128">-DeviceName</span></span>
<span data-ttu-id="7d3b4-129">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="7d3b4-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3b4-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d3b4-130">-InputObject</span></span>
<span data-ttu-id="7d3b4-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d3b4-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3b4-132">-Name</span><span class="sxs-lookup"><span data-stu-id="7d3b4-132">-Name</span></span>
<span data-ttu-id="7d3b4-133">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="7d3b4-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3b4-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d3b4-134">-ResourceGroupName</span></span>
<span data-ttu-id="7d3b4-135">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7d3b4-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3b4-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d3b4-136">-ResourceId</span></span>
<span data-ttu-id="7d3b4-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d3b4-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3b4-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7d3b4-138">-StartTime</span></span>
<span data-ttu-id="7d3b4-139">Запланировать время начала</span><span class="sxs-lookup"><span data-stu-id="7d3b4-139">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3b4-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="7d3b4-140">-StopTime</span></span>
<span data-ttu-id="7d3b4-141">Время остановки по расписанию</span><span class="sxs-lookup"><span data-stu-id="7d3b4-141">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3b4-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="7d3b4-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="7d3b4-143">Будет установлена безлимитная пропускная способность</span><span class="sxs-lookup"><span data-stu-id="7d3b4-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d3b4-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d3b4-144">-Confirm</span></span>
<span data-ttu-id="7d3b4-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d3b4-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d3b4-146">-WhatIf</span></span>
<span data-ttu-id="7d3b4-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d3b4-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d3b4-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d3b4-149">CommonParameters</span></span>
<span data-ttu-id="7d3b4-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d3b4-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d3b4-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7d3b4-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d3b4-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7d3b4-152">INPUTS</span></span>

### <span data-ttu-id="7d3b4-153">Нет</span><span class="sxs-lookup"><span data-stu-id="7d3b4-153">None</span></span>

## <span data-ttu-id="7d3b4-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7d3b4-154">OUTPUTS</span></span>

### <span data-ttu-id="7d3b4-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="7d3b4-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="7d3b4-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7d3b4-156">NOTES</span></span>

## <span data-ttu-id="7d3b4-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d3b4-157">RELATED LINKS</span></span>
