---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228932"
---
# <span data-ttu-id="f07f8-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="f07f8-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="f07f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f07f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f07f8-103">Обновляет расписание пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="f07f8-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="f07f8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f07f8-104">SYNTAX</span></span>

### <span data-ttu-id="f07f8-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f07f8-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f07f8-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f07f8-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f07f8-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="f07f8-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f07f8-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="f07f8-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f07f8-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f07f8-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f07f8-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="f07f8-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f07f8-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="f07f8-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f07f8-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="f07f8-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f07f8-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="f07f8-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f07f8-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f07f8-114">DESCRIPTION</span></span>
<span data-ttu-id="f07f8-115">**Cmdlet Set-AzDataBoxEdgeBandwidthSchedule** обновляет расписание пропускной способности для устройства Edge data Box.</span><span class="sxs-lookup"><span data-stu-id="f07f8-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="f07f8-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f07f8-116">EXAMPLES</span></span>

### <span data-ttu-id="f07f8-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f07f8-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="f07f8-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f07f8-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="f07f8-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f07f8-119">PARAMETERS</span></span>

### <span data-ttu-id="f07f8-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f07f8-120">-AsJob</span></span>
<span data-ttu-id="f07f8-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f07f8-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f07f8-122">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="f07f8-122">-Bandwidth</span></span>
<span data-ttu-id="f07f8-123">Пропускная способность в Мбит/с</span><span class="sxs-lookup"><span data-stu-id="f07f8-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="f07f8-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="f07f8-124">-DaysOfWeek</span></span>
<span data-ttu-id="f07f8-125">Запланированные дниOfWeek</span><span class="sxs-lookup"><span data-stu-id="f07f8-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="f07f8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f07f8-126">-DefaultProfile</span></span>
<span data-ttu-id="f07f8-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f07f8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f07f8-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="f07f8-128">-DeviceName</span></span>
<span data-ttu-id="f07f8-129">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="f07f8-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07f8-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f07f8-130">-InputObject</span></span>
<span data-ttu-id="f07f8-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f07f8-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07f8-132">-Name</span><span class="sxs-lookup"><span data-stu-id="f07f8-132">-Name</span></span>
<span data-ttu-id="f07f8-133">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="f07f8-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07f8-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f07f8-134">-ResourceGroupName</span></span>
<span data-ttu-id="f07f8-135">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f07f8-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07f8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f07f8-136">-ResourceId</span></span>
<span data-ttu-id="f07f8-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="f07f8-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07f8-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f07f8-138">-StartTime</span></span>
<span data-ttu-id="f07f8-139">Запланировать время начала</span><span class="sxs-lookup"><span data-stu-id="f07f8-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="f07f8-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="f07f8-140">-StopTime</span></span>
<span data-ttu-id="f07f8-141">Время остановки по расписанию</span><span class="sxs-lookup"><span data-stu-id="f07f8-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="f07f8-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="f07f8-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="f07f8-143">Будет настроена безлимитная пропускная способность</span><span class="sxs-lookup"><span data-stu-id="f07f8-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f07f8-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f07f8-144">-Confirm</span></span>
<span data-ttu-id="f07f8-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f07f8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f07f8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f07f8-146">-WhatIf</span></span>
<span data-ttu-id="f07f8-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f07f8-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f07f8-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f07f8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f07f8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f07f8-149">CommonParameters</span></span>
<span data-ttu-id="f07f8-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f07f8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f07f8-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f07f8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f07f8-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f07f8-152">INPUTS</span></span>

### <span data-ttu-id="f07f8-153">Нет</span><span class="sxs-lookup"><span data-stu-id="f07f8-153">None</span></span>

## <span data-ttu-id="f07f8-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f07f8-154">OUTPUTS</span></span>

### <span data-ttu-id="f07f8-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="f07f8-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="f07f8-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f07f8-156">NOTES</span></span>

## <span data-ttu-id="f07f8-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f07f8-157">RELATED LINKS</span></span>
