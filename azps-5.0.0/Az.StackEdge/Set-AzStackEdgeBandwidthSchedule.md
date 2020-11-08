---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247208"
---
# <span data-ttu-id="dba16-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="dba16-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="dba16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dba16-102">SYNOPSIS</span></span>
<span data-ttu-id="dba16-103">Обновление расписания пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="dba16-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="dba16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dba16-104">SYNTAX</span></span>

### <span data-ttu-id="dba16-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dba16-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba16-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dba16-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dba16-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dba16-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba16-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dba16-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba16-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dba16-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba16-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dba16-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba16-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dba16-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba16-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dba16-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba16-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="dba16-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dba16-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dba16-114">DESCRIPTION</span></span>
<span data-ttu-id="dba16-115">Командлет **Set-AzStackEdgeBandwidthSchedule** обновляет расписание пропускной способности для краевого устройства стека.</span><span class="sxs-lookup"><span data-stu-id="dba16-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="dba16-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dba16-116">EXAMPLES</span></span>

### <span data-ttu-id="dba16-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dba16-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="dba16-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dba16-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="dba16-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dba16-119">PARAMETERS</span></span>

### <span data-ttu-id="dba16-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dba16-120">-AsJob</span></span>
<span data-ttu-id="dba16-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dba16-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dba16-122">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="dba16-122">-Bandwidth</span></span>
<span data-ttu-id="dba16-123">Пропускная способность в Мбит/с</span><span class="sxs-lookup"><span data-stu-id="dba16-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="dba16-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="dba16-124">-DaysOfWeek</span></span>
<span data-ttu-id="dba16-125">Запланированные DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="dba16-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="dba16-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba16-126">-DefaultProfile</span></span>
<span data-ttu-id="dba16-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dba16-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dba16-128">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="dba16-128">-DeviceName</span></span>
<span data-ttu-id="dba16-129">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="dba16-129">Device Name</span></span>

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

### <span data-ttu-id="dba16-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dba16-130">-InputObject</span></span>
<span data-ttu-id="dba16-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="dba16-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="dba16-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dba16-132">-Name</span></span>
<span data-ttu-id="dba16-133">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="dba16-133">Resource Name</span></span>

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

### <span data-ttu-id="dba16-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba16-134">-ResourceGroupName</span></span>
<span data-ttu-id="dba16-135">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="dba16-135">Resource Group Name</span></span>

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

### <span data-ttu-id="dba16-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dba16-136">-ResourceId</span></span>
<span data-ttu-id="dba16-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="dba16-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="dba16-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dba16-138">-StartTime</span></span>
<span data-ttu-id="dba16-139">Время начала расписания</span><span class="sxs-lookup"><span data-stu-id="dba16-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="dba16-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="dba16-140">-StopTime</span></span>
<span data-ttu-id="dba16-141">Время остановки расписания</span><span class="sxs-lookup"><span data-stu-id="dba16-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="dba16-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="dba16-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="dba16-143">Будет настроена неограниченная пропускная способность</span><span class="sxs-lookup"><span data-stu-id="dba16-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="dba16-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dba16-144">-Confirm</span></span>
<span data-ttu-id="dba16-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dba16-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dba16-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dba16-146">-WhatIf</span></span>
<span data-ttu-id="dba16-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dba16-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dba16-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dba16-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dba16-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba16-149">CommonParameters</span></span>
<span data-ttu-id="dba16-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dba16-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba16-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dba16-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba16-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dba16-152">INPUTS</span></span>

### <span data-ttu-id="dba16-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="dba16-153">None</span></span>

## <span data-ttu-id="dba16-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dba16-154">OUTPUTS</span></span>

### <span data-ttu-id="dba16-155">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="dba16-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="dba16-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="dba16-156">NOTES</span></span>

## <span data-ttu-id="dba16-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dba16-157">RELATED LINKS</span></span>
