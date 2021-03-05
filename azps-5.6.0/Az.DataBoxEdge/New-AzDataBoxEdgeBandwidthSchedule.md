---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 2c83773ba08c2fefe9404fa69861518d00d4d936
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998052"
---
# <span data-ttu-id="80cca-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="80cca-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="80cca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80cca-102">SYNOPSIS</span></span>
<span data-ttu-id="80cca-103">Создание нового расписания пропускной способности</span><span class="sxs-lookup"><span data-stu-id="80cca-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="80cca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="80cca-104">SYNTAX</span></span>

### <span data-ttu-id="80cca-105">BandwidthParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="80cca-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80cca-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="80cca-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80cca-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80cca-107">DESCRIPTION</span></span>
<span data-ttu-id="80cca-108">С **помощью cmdlet New-AzDataBoxEdgeBandwidthSchedule** создается новое расписание полосы пропускания для устройства Edge Data Box, помогающее управлять использованием полосы пропускания.</span><span class="sxs-lookup"><span data-stu-id="80cca-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="80cca-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="80cca-109">EXAMPLES</span></span>

### <span data-ttu-id="80cca-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="80cca-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="80cca-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="80cca-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="80cca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80cca-112">PARAMETERS</span></span>

### <span data-ttu-id="80cca-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80cca-113">-AsJob</span></span>
<span data-ttu-id="80cca-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="80cca-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80cca-115">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="80cca-115">-Bandwidth</span></span>
<span data-ttu-id="80cca-116">Пропускная способность в Мбит/с</span><span class="sxs-lookup"><span data-stu-id="80cca-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="80cca-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="80cca-117">-DaysOfWeek</span></span>
<span data-ttu-id="80cca-118">Запланированные дниOfWeek</span><span class="sxs-lookup"><span data-stu-id="80cca-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="80cca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80cca-119">-DefaultProfile</span></span>
<span data-ttu-id="80cca-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80cca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80cca-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="80cca-121">-DeviceName</span></span>
<span data-ttu-id="80cca-122">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="80cca-122">Device Name</span></span>

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

### <span data-ttu-id="80cca-123">-Name</span><span class="sxs-lookup"><span data-stu-id="80cca-123">-Name</span></span>
<span data-ttu-id="80cca-124">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="80cca-124">Resource Name</span></span>

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

### <span data-ttu-id="80cca-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80cca-125">-ResourceGroupName</span></span>
<span data-ttu-id="80cca-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="80cca-126">Resource Group Name</span></span>

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

### <span data-ttu-id="80cca-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="80cca-127">-StartTime</span></span>
<span data-ttu-id="80cca-128">Запланировать время начала</span><span class="sxs-lookup"><span data-stu-id="80cca-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="80cca-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="80cca-129">-StopTime</span></span>
<span data-ttu-id="80cca-130">Время остановки по расписанию</span><span class="sxs-lookup"><span data-stu-id="80cca-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="80cca-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="80cca-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="80cca-132">Будет установлена безлимитная пропускная способность, если установлено значение false , будет установлено значение по умолчанию 20 Мбит/с</span><span class="sxs-lookup"><span data-stu-id="80cca-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

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

### <span data-ttu-id="80cca-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80cca-133">-Confirm</span></span>
<span data-ttu-id="80cca-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80cca-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80cca-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80cca-135">-WhatIf</span></span>
<span data-ttu-id="80cca-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80cca-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80cca-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="80cca-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80cca-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80cca-138">CommonParameters</span></span>
<span data-ttu-id="80cca-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80cca-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80cca-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80cca-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80cca-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80cca-141">INPUTS</span></span>

### <span data-ttu-id="80cca-142">Нет</span><span class="sxs-lookup"><span data-stu-id="80cca-142">None</span></span>

## <span data-ttu-id="80cca-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="80cca-143">OUTPUTS</span></span>

### <span data-ttu-id="80cca-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="80cca-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="80cca-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="80cca-145">NOTES</span></span>

## <span data-ttu-id="80cca-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80cca-146">RELATED LINKS</span></span>
