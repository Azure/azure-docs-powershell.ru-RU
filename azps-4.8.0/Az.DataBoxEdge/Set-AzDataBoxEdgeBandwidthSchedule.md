---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244588"
---
# <span data-ttu-id="15663-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="15663-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="15663-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15663-102">SYNOPSIS</span></span>
<span data-ttu-id="15663-103">Обновление расписания пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="15663-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="15663-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15663-104">SYNTAX</span></span>

### <span data-ttu-id="15663-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15663-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15663-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15663-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15663-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="15663-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15663-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="15663-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15663-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15663-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15663-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="15663-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15663-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="15663-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15663-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="15663-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15663-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="15663-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15663-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15663-114">DESCRIPTION</span></span>
<span data-ttu-id="15663-115">Командлет **Set-AzDataBoxEdgeBandwidthSchedule** обновляет расписание пропускной способности для пограничного устройства поля данных.</span><span class="sxs-lookup"><span data-stu-id="15663-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="15663-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15663-116">EXAMPLES</span></span>

### <span data-ttu-id="15663-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="15663-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="15663-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="15663-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="15663-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15663-119">PARAMETERS</span></span>

### <span data-ttu-id="15663-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15663-120">-AsJob</span></span>
<span data-ttu-id="15663-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="15663-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15663-122">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="15663-122">-Bandwidth</span></span>
<span data-ttu-id="15663-123">Пропускная способность в Мбит/с</span><span class="sxs-lookup"><span data-stu-id="15663-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="15663-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="15663-124">-DaysOfWeek</span></span>
<span data-ttu-id="15663-125">Запланированные DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="15663-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="15663-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15663-126">-DefaultProfile</span></span>
<span data-ttu-id="15663-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15663-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15663-128">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="15663-128">-DeviceName</span></span>
<span data-ttu-id="15663-129">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="15663-129">Device Name</span></span>

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

### <span data-ttu-id="15663-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15663-130">-InputObject</span></span>
<span data-ttu-id="15663-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="15663-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="15663-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15663-132">-Name</span></span>
<span data-ttu-id="15663-133">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="15663-133">Resource Name</span></span>

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

### <span data-ttu-id="15663-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15663-134">-ResourceGroupName</span></span>
<span data-ttu-id="15663-135">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="15663-135">Resource Group Name</span></span>

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

### <span data-ttu-id="15663-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15663-136">-ResourceId</span></span>
<span data-ttu-id="15663-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="15663-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="15663-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="15663-138">-StartTime</span></span>
<span data-ttu-id="15663-139">Время начала расписания</span><span class="sxs-lookup"><span data-stu-id="15663-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="15663-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="15663-140">-StopTime</span></span>
<span data-ttu-id="15663-141">Время остановки расписания</span><span class="sxs-lookup"><span data-stu-id="15663-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="15663-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="15663-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="15663-143">Будет настроена неограниченная пропускная способность</span><span class="sxs-lookup"><span data-stu-id="15663-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="15663-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15663-144">-Confirm</span></span>
<span data-ttu-id="15663-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15663-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15663-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15663-146">-WhatIf</span></span>
<span data-ttu-id="15663-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15663-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15663-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15663-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15663-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15663-149">CommonParameters</span></span>
<span data-ttu-id="15663-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15663-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15663-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15663-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15663-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15663-152">INPUTS</span></span>

### <span data-ttu-id="15663-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="15663-153">None</span></span>

## <span data-ttu-id="15663-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15663-154">OUTPUTS</span></span>

### <span data-ttu-id="15663-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="15663-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="15663-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="15663-156">NOTES</span></span>

## <span data-ttu-id="15663-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15663-157">RELATED LINKS</span></span>
