---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e15e6ee6186dc19f9f85264548c1b735ea242b98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911271"
---
# <span data-ttu-id="bc274-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="bc274-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="bc274-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc274-102">SYNOPSIS</span></span>
<span data-ttu-id="bc274-103">Создание нового расписания пропускной способности</span><span class="sxs-lookup"><span data-stu-id="bc274-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="bc274-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc274-104">SYNTAX</span></span>

### <span data-ttu-id="bc274-105">BandwidthParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bc274-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc274-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc274-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc274-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc274-107">DESCRIPTION</span></span>
<span data-ttu-id="bc274-108">Командлет **New-AzDataBoxEdgeBandwidthSchedule** создает новое расписание пропускной способности для поля с пограничным устройством, которое помогает управлять использованием пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="bc274-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="bc274-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc274-109">EXAMPLES</span></span>

### <span data-ttu-id="bc274-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc274-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="bc274-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bc274-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="bc274-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc274-112">PARAMETERS</span></span>

### <span data-ttu-id="bc274-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc274-113">-AsJob</span></span>
<span data-ttu-id="bc274-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bc274-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc274-115">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="bc274-115">-Bandwidth</span></span>
<span data-ttu-id="bc274-116">Пропускная способность в Мбит/с</span><span class="sxs-lookup"><span data-stu-id="bc274-116">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: BandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc274-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="bc274-117">-DaysOfWeek</span></span>
<span data-ttu-id="bc274-118">Запланированные DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="bc274-118">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc274-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc274-119">-DefaultProfile</span></span>
<span data-ttu-id="bc274-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc274-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc274-121">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="bc274-121">-DeviceName</span></span>
<span data-ttu-id="bc274-122">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="bc274-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc274-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc274-123">-Name</span></span>
<span data-ttu-id="bc274-124">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="bc274-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc274-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc274-125">-ResourceGroupName</span></span>
<span data-ttu-id="bc274-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bc274-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc274-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bc274-127">-StartTime</span></span>
<span data-ttu-id="bc274-128">Время начала расписания</span><span class="sxs-lookup"><span data-stu-id="bc274-128">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc274-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="bc274-129">-StopTime</span></span>
<span data-ttu-id="bc274-130">Время остановки расписания</span><span class="sxs-lookup"><span data-stu-id="bc274-130">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc274-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="bc274-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="bc274-132">Задаст неограниченную пропускную способность, если для параметра "ложь" задано значение по умолчанию 20 Мбит/с</span><span class="sxs-lookup"><span data-stu-id="bc274-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc274-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc274-133">-Confirm</span></span>
<span data-ttu-id="bc274-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bc274-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc274-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc274-135">-WhatIf</span></span>
<span data-ttu-id="bc274-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bc274-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc274-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc274-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc274-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc274-138">CommonParameters</span></span>
<span data-ttu-id="bc274-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc274-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc274-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc274-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc274-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc274-141">INPUTS</span></span>

### <span data-ttu-id="bc274-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="bc274-142">None</span></span>

## <span data-ttu-id="bc274-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc274-143">OUTPUTS</span></span>

### <span data-ttu-id="bc274-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="bc274-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="bc274-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc274-145">NOTES</span></span>

## <span data-ttu-id="bc274-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc274-146">RELATED LINKS</span></span>
