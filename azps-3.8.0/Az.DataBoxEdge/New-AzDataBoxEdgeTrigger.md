---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: ac7fb7d6af2e04387ea4abfa3fe62c4df9271b13
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072811"
---
# <span data-ttu-id="f0ca8-101">New-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="f0ca8-101">New-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="f0ca8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ca8-103">Настройка триггера на устройстве.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="f0ca8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0ca8-104">SYNTAX</span></span>

### <span data-ttu-id="f0ca8-105">FileEventTriggerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0ca8-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0ca8-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0ca8-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0ca8-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0ca8-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0ca8-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0ca8-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0ca8-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0ca8-109">DESCRIPTION</span></span>
<span data-ttu-id="f0ca8-110">Командлет **New-AzDataBoxEdgeTrigger** настраивает триггер на пограничном устройстве поля данных.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-110">The **New-AzDataBoxEdgeTrigger** cmdlet configures a trigger on the Data Box Edge device.</span></span> 

## <span data-ttu-id="f0ca8-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0ca8-111">EXAMPLES</span></span>

### <span data-ttu-id="f0ca8-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0ca8-112">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="f0ca8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0ca8-113">PARAMETERS</span></span>

### <span data-ttu-id="f0ca8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0ca8-114">-AsJob</span></span>
<span data-ttu-id="f0ca8-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f0ca8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0ca8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ca8-116">-DefaultProfile</span></span>
<span data-ttu-id="f0ca8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0ca8-118">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="f0ca8-118">-DeviceName</span></span>
<span data-ttu-id="f0ca8-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="f0ca8-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca8-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="f0ca8-120">-FileEvent</span></span>
<span data-ttu-id="f0ca8-121">Передайте этот параметр для настройки триггера FileEvent</span><span class="sxs-lookup"><span data-stu-id="f0ca8-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileEventTriggerParameterSet, FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca8-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0ca8-122">-Name</span></span>
<span data-ttu-id="f0ca8-123">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="f0ca8-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca8-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="f0ca8-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="f0ca8-125">Передайте этот параметр для настройки триггера PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="f0ca8-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0ca8-126">-ResourceGroupName</span></span>
<span data-ttu-id="f0ca8-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0ca8-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca8-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="f0ca8-128">-RoleName</span></span>
<span data-ttu-id="f0ca8-129">Вычислите роль, в которой будут инициироваться события.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-129">Compute role against which events will be raised.</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca8-130">-Планирование</span><span class="sxs-lookup"><span data-stu-id="f0ca8-130">-Schedule</span></span>
<span data-ttu-id="f0ca8-131">Периодическая частота, на которую необходимо инициировать событие таймера.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="f0ca8-132">Расписание можно задать в днях (от 1 до 365), часов (от 1 до 23) или минут (от 1 до 59).</span><span class="sxs-lookup"><span data-stu-id="f0ca8-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca8-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="f0ca8-133">-ShareId</span></span>
<span data-ttu-id="f0ca8-134">ИД общего файлового файла, который должен быть передан в триггере FileEvent</span><span class="sxs-lookup"><span data-stu-id="f0ca8-134">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca8-135">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="f0ca8-135">-ShareName</span></span>
<span data-ttu-id="f0ca8-136">ИД общего файлового файла, который должен быть передан в триггере FileEvent</span><span class="sxs-lookup"><span data-stu-id="f0ca8-136">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca8-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f0ca8-137">-StartTime</span></span>
<span data-ttu-id="f0ca8-138">Время суток, в которое получен допустимый триггер.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="f0ca8-139">Расписание вычисляется ссылкой на время, указанное до секунд.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="f0ca8-140">Если TimeZone не указан, время будет считаться часовым поясом устройства.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="f0ca8-141">Значение всегда будет возвращаться как время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-141">The value will always be returned as UTC time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca8-142">-Темы</span><span class="sxs-lookup"><span data-stu-id="f0ca8-142">-Topic</span></span>
<span data-ttu-id="f0ca8-143">Раздел, в котором периодически публикуются события на устройстве IoT.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-143">Topic where periodic events are published to IoT device.</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0ca8-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0ca8-144">-Confirm</span></span>
<span data-ttu-id="f0ca8-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0ca8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ca8-146">-WhatIf</span></span>
<span data-ttu-id="f0ca8-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0ca8-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0ca8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ca8-149">CommonParameters</span></span>
<span data-ttu-id="f0ca8-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0ca8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ca8-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0ca8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ca8-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0ca8-152">INPUTS</span></span>

### <span data-ttu-id="f0ca8-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="f0ca8-153">None</span></span>

## <span data-ttu-id="f0ca8-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0ca8-154">OUTPUTS</span></span>

### <span data-ttu-id="f0ca8-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="f0ca8-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="f0ca8-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0ca8-156">NOTES</span></span>

## <span data-ttu-id="f0ca8-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0ca8-157">RELATED LINKS</span></span>
