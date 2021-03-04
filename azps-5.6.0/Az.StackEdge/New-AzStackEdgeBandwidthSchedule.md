---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: a9a49f89301da627fcafa285915d0331240f75b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982003"
---
# <span data-ttu-id="b0a98-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b0a98-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="b0a98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0a98-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a98-103">Создание нового расписания пропускной способности</span><span class="sxs-lookup"><span data-stu-id="b0a98-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="b0a98-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0a98-104">SYNTAX</span></span>

### <span data-ttu-id="b0a98-105">UnlimitedBandwidthParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b0a98-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0a98-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0a98-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0a98-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0a98-107">DESCRIPTION</span></span>
<span data-ttu-id="b0a98-108">С **помощью cmdlet New-AzStackEdgeBandwidthSchedule** создается новое расписание пропускной способности для устройства Stack Edge, помогающее управлять использованием полосы пропускания.</span><span class="sxs-lookup"><span data-stu-id="b0a98-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="b0a98-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0a98-109">EXAMPLES</span></span>

### <span data-ttu-id="b0a98-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b0a98-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="b0a98-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b0a98-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="b0a98-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0a98-112">PARAMETERS</span></span>

### <span data-ttu-id="b0a98-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0a98-113">-AsJob</span></span>
<span data-ttu-id="b0a98-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b0a98-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0a98-115">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="b0a98-115">-Bandwidth</span></span>
<span data-ttu-id="b0a98-116">Пропускная способность в Мбит/с</span><span class="sxs-lookup"><span data-stu-id="b0a98-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="b0a98-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="b0a98-117">-DaysOfWeek</span></span>
<span data-ttu-id="b0a98-118">Запланированные дниOfWeek</span><span class="sxs-lookup"><span data-stu-id="b0a98-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="b0a98-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a98-119">-DefaultProfile</span></span>
<span data-ttu-id="b0a98-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0a98-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0a98-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b0a98-121">-DeviceName</span></span>
<span data-ttu-id="b0a98-122">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="b0a98-122">Device Name</span></span>

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

### <span data-ttu-id="b0a98-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b0a98-123">-Name</span></span>
<span data-ttu-id="b0a98-124">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="b0a98-124">Resource Name</span></span>

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

### <span data-ttu-id="b0a98-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0a98-125">-ResourceGroupName</span></span>
<span data-ttu-id="b0a98-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b0a98-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b0a98-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b0a98-127">-StartTime</span></span>
<span data-ttu-id="b0a98-128">Запланировать время начала</span><span class="sxs-lookup"><span data-stu-id="b0a98-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="b0a98-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="b0a98-129">-StopTime</span></span>
<span data-ttu-id="b0a98-130">Время остановки по расписанию</span><span class="sxs-lookup"><span data-stu-id="b0a98-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="b0a98-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="b0a98-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="b0a98-132">Будет установлено значение "Без ограничений" для полосы пропускания</span><span class="sxs-lookup"><span data-stu-id="b0a98-132">Will Set Bandwidth as Unlimited</span></span>

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

### <span data-ttu-id="b0a98-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0a98-133">-Confirm</span></span>
<span data-ttu-id="b0a98-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0a98-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0a98-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0a98-135">-WhatIf</span></span>
<span data-ttu-id="b0a98-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0a98-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0a98-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b0a98-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0a98-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a98-138">CommonParameters</span></span>
<span data-ttu-id="b0a98-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0a98-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a98-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0a98-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a98-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0a98-141">INPUTS</span></span>

### <span data-ttu-id="b0a98-142">Нет</span><span class="sxs-lookup"><span data-stu-id="b0a98-142">None</span></span>

## <span data-ttu-id="b0a98-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0a98-143">OUTPUTS</span></span>

### <span data-ttu-id="b0a98-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="b0a98-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="b0a98-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0a98-145">NOTES</span></span>

## <span data-ttu-id="b0a98-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0a98-146">RELATED LINKS</span></span>
