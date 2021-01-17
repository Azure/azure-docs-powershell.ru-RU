---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413415"
---
# <span data-ttu-id="10390-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="10390-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="10390-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10390-102">SYNOPSIS</span></span>
<span data-ttu-id="10390-103">Создание нового расписания пропускной способности</span><span class="sxs-lookup"><span data-stu-id="10390-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="10390-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="10390-104">SYNTAX</span></span>

### <span data-ttu-id="10390-105">UnlimitedBandwidthParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="10390-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10390-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="10390-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10390-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10390-107">DESCRIPTION</span></span>
<span data-ttu-id="10390-108">С **помощью cmdlet New-AzStackEdgeBandwidthSchedule** создается новое расписание полосы пропускания для устройства Stack Edge, помогающее управлять использованием полосы пропускания.</span><span class="sxs-lookup"><span data-stu-id="10390-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="10390-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="10390-109">EXAMPLES</span></span>

### <span data-ttu-id="10390-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="10390-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="10390-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="10390-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="10390-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10390-112">PARAMETERS</span></span>

### <span data-ttu-id="10390-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="10390-113">-AsJob</span></span>
<span data-ttu-id="10390-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="10390-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="10390-115">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="10390-115">-Bandwidth</span></span>
<span data-ttu-id="10390-116">Пропускная способность в Мбит/с</span><span class="sxs-lookup"><span data-stu-id="10390-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="10390-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="10390-117">-DaysOfWeek</span></span>
<span data-ttu-id="10390-118">Запланированные дниOfWeek</span><span class="sxs-lookup"><span data-stu-id="10390-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="10390-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10390-119">-DefaultProfile</span></span>
<span data-ttu-id="10390-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10390-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10390-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="10390-121">-DeviceName</span></span>
<span data-ttu-id="10390-122">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="10390-122">Device Name</span></span>

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

### <span data-ttu-id="10390-123">-Name</span><span class="sxs-lookup"><span data-stu-id="10390-123">-Name</span></span>
<span data-ttu-id="10390-124">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="10390-124">Resource Name</span></span>

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

### <span data-ttu-id="10390-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10390-125">-ResourceGroupName</span></span>
<span data-ttu-id="10390-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="10390-126">Resource Group Name</span></span>

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

### <span data-ttu-id="10390-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="10390-127">-StartTime</span></span>
<span data-ttu-id="10390-128">Запланировать время начала</span><span class="sxs-lookup"><span data-stu-id="10390-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="10390-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="10390-129">-StopTime</span></span>
<span data-ttu-id="10390-130">Время остановки по расписанию</span><span class="sxs-lookup"><span data-stu-id="10390-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="10390-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="10390-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="10390-132">Будет установлено значение "Без ограничений" для полосы пропускания</span><span class="sxs-lookup"><span data-stu-id="10390-132">Will Set Bandwidth as Unlimited</span></span>

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

### <span data-ttu-id="10390-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10390-133">-Confirm</span></span>
<span data-ttu-id="10390-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="10390-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10390-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10390-135">-WhatIf</span></span>
<span data-ttu-id="10390-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10390-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10390-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="10390-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10390-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10390-138">CommonParameters</span></span>
<span data-ttu-id="10390-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10390-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10390-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10390-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10390-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10390-141">INPUTS</span></span>

### <span data-ttu-id="10390-142">Нет</span><span class="sxs-lookup"><span data-stu-id="10390-142">None</span></span>

## <span data-ttu-id="10390-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="10390-143">OUTPUTS</span></span>

### <span data-ttu-id="10390-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="10390-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="10390-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="10390-145">NOTES</span></span>

## <span data-ttu-id="10390-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10390-146">RELATED LINKS</span></span>
