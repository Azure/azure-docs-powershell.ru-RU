---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235745"
---
# <span data-ttu-id="304af-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="304af-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="304af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="304af-102">SYNOPSIS</span></span>
<span data-ttu-id="304af-103">Создание нового расписания пропускной способности</span><span class="sxs-lookup"><span data-stu-id="304af-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="304af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="304af-104">SYNTAX</span></span>

### <span data-ttu-id="304af-105">UnlimitedBandwidthParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="304af-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="304af-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="304af-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="304af-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="304af-107">DESCRIPTION</span></span>
<span data-ttu-id="304af-108">Командлет **New-AzStackEdgeBandwidthSchedule** создает новое расписание пропускной способности для краевого устройства стека, что помогает управлять использованием пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="304af-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="304af-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="304af-109">EXAMPLES</span></span>

### <span data-ttu-id="304af-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="304af-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="304af-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="304af-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="304af-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="304af-112">PARAMETERS</span></span>

### <span data-ttu-id="304af-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="304af-113">-AsJob</span></span>
<span data-ttu-id="304af-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="304af-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="304af-115">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="304af-115">-Bandwidth</span></span>
<span data-ttu-id="304af-116">Пропускная способность в Мбит/с</span><span class="sxs-lookup"><span data-stu-id="304af-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="304af-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="304af-117">-DaysOfWeek</span></span>
<span data-ttu-id="304af-118">Запланированные DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="304af-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="304af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="304af-119">-DefaultProfile</span></span>
<span data-ttu-id="304af-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="304af-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="304af-121">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="304af-121">-DeviceName</span></span>
<span data-ttu-id="304af-122">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="304af-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="304af-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="304af-123">-Name</span></span>
<span data-ttu-id="304af-124">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="304af-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304af-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="304af-125">-ResourceGroupName</span></span>
<span data-ttu-id="304af-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="304af-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="304af-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="304af-127">-StartTime</span></span>
<span data-ttu-id="304af-128">Время начала расписания</span><span class="sxs-lookup"><span data-stu-id="304af-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="304af-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="304af-129">-StopTime</span></span>
<span data-ttu-id="304af-130">Время остановки расписания</span><span class="sxs-lookup"><span data-stu-id="304af-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="304af-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="304af-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="304af-132">Настройка пропускной способности не ограничена</span><span class="sxs-lookup"><span data-stu-id="304af-132">Will Set Bandwidth as Unlimited</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304af-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="304af-133">-Confirm</span></span>
<span data-ttu-id="304af-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="304af-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="304af-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="304af-135">-WhatIf</span></span>
<span data-ttu-id="304af-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="304af-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="304af-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="304af-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="304af-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304af-138">CommonParameters</span></span>
<span data-ttu-id="304af-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="304af-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304af-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="304af-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304af-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="304af-141">INPUTS</span></span>

### <span data-ttu-id="304af-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="304af-142">None</span></span>

## <span data-ttu-id="304af-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="304af-143">OUTPUTS</span></span>

### <span data-ttu-id="304af-144">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="304af-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="304af-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="304af-145">NOTES</span></span>

## <span data-ttu-id="304af-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="304af-146">RELATED LINKS</span></span>
