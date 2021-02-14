---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: ac7fb7d6af2e04387ea4abfa3fe62c4df9271b13
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215153"
---
# <span data-ttu-id="b9ccd-101">New-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="b9ccd-101">New-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="b9ccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ccd-103">Настраивает триггер на устройстве.</span><span class="sxs-lookup"><span data-stu-id="b9ccd-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="b9ccd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b9ccd-104">SYNTAX</span></span>

### <span data-ttu-id="b9ccd-105">FileEventTriggerParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9ccd-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9ccd-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9ccd-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9ccd-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9ccd-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9ccd-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9ccd-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9ccd-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9ccd-109">DESCRIPTION</span></span>
<span data-ttu-id="b9ccd-110">Для настройки триггера На устройстве Data Box Edge будет настроен триггер **New-AzDataBoxEdgeTrigger.**</span><span class="sxs-lookup"><span data-stu-id="b9ccd-110">The **New-AzDataBoxEdgeTrigger** cmdlet configures a trigger on the Data Box Edge device.</span></span> 

## <span data-ttu-id="b9ccd-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b9ccd-111">EXAMPLES</span></span>

### <span data-ttu-id="b9ccd-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9ccd-112">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="b9ccd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9ccd-113">PARAMETERS</span></span>

### <span data-ttu-id="b9ccd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9ccd-114">-AsJob</span></span>
<span data-ttu-id="b9ccd-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b9ccd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9ccd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ccd-116">-DefaultProfile</span></span>
<span data-ttu-id="b9ccd-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ccd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9ccd-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b9ccd-118">-DeviceName</span></span>
<span data-ttu-id="b9ccd-119">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="b9ccd-119">Device Name</span></span>

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

### <span data-ttu-id="b9ccd-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="b9ccd-120">-FileEvent</span></span>
<span data-ttu-id="b9ccd-121">Передать этот параметр переключения для настройки триггера FileEvent</span><span class="sxs-lookup"><span data-stu-id="b9ccd-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

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

### <span data-ttu-id="b9ccd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b9ccd-122">-Name</span></span>
<span data-ttu-id="b9ccd-123">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="b9ccd-123">Resource Name</span></span>

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

### <span data-ttu-id="b9ccd-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="b9ccd-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="b9ccd-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span><span class="sxs-lookup"><span data-stu-id="b9ccd-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

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

### <span data-ttu-id="b9ccd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9ccd-126">-ResourceGroupName</span></span>
<span data-ttu-id="b9ccd-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b9ccd-127">Resource Group Name</span></span>

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

### <span data-ttu-id="b9ccd-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="b9ccd-128">-RoleName</span></span>
<span data-ttu-id="b9ccd-129">Вычислять роль, с которой будут соединимы события.</span><span class="sxs-lookup"><span data-stu-id="b9ccd-129">Compute role against which events will be raised.</span></span>

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

### <span data-ttu-id="b9ccd-130">-Расписание</span><span class="sxs-lookup"><span data-stu-id="b9ccd-130">-Schedule</span></span>
<span data-ttu-id="b9ccd-131">Периодическая частота, при которой требуется повысить время ожидания.</span><span class="sxs-lookup"><span data-stu-id="b9ccd-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="b9ccd-132">Укажите расписание в днях (от 1 до 365), часах (от 1 до 23) или минутах (от 1 до 59).</span><span class="sxs-lookup"><span data-stu-id="b9ccd-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

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

### <span data-ttu-id="b9ccd-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="b9ccd-133">-ShareId</span></span>
<span data-ttu-id="b9ccd-134">File share ID to be passed in FileEvent Trigger</span><span class="sxs-lookup"><span data-stu-id="b9ccd-134">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="b9ccd-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b9ccd-135">-ShareName</span></span>
<span data-ttu-id="b9ccd-136">File share ID to be passed in FileEvent Trigger</span><span class="sxs-lookup"><span data-stu-id="b9ccd-136">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="b9ccd-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b9ccd-137">-StartTime</span></span>
<span data-ttu-id="b9ccd-138">Время дня, которое приводит к действительному триггеру.</span><span class="sxs-lookup"><span data-stu-id="b9ccd-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="b9ccd-139">Для расчета расписания указывается время (до секунд).</span><span class="sxs-lookup"><span data-stu-id="b9ccd-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="b9ccd-140">Если часовой пояс не указан, время будет указано в часовом поясе устройства.</span><span class="sxs-lookup"><span data-stu-id="b9ccd-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="b9ccd-141">Значение всегда возвращается в качестве времени в UTC.</span><span class="sxs-lookup"><span data-stu-id="b9ccd-141">The value will always be returned as UTC time.</span></span>

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

### <span data-ttu-id="b9ccd-142">-Topic</span><span class="sxs-lookup"><span data-stu-id="b9ccd-142">-Topic</span></span>
<span data-ttu-id="b9ccd-143">Раздел, в котором периодические события публикуются на устройстве IoT.</span><span class="sxs-lookup"><span data-stu-id="b9ccd-143">Topic where periodic events are published to IoT device.</span></span>

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

### <span data-ttu-id="b9ccd-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9ccd-144">-Confirm</span></span>
<span data-ttu-id="b9ccd-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9ccd-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9ccd-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9ccd-146">-WhatIf</span></span>
<span data-ttu-id="b9ccd-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9ccd-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9ccd-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b9ccd-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9ccd-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ccd-149">CommonParameters</span></span>
<span data-ttu-id="b9ccd-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ccd-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ccd-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9ccd-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ccd-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9ccd-152">INPUTS</span></span>

### <span data-ttu-id="b9ccd-153">Нет</span><span class="sxs-lookup"><span data-stu-id="b9ccd-153">None</span></span>

## <span data-ttu-id="b9ccd-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9ccd-154">OUTPUTS</span></span>

### <span data-ttu-id="b9ccd-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="b9ccd-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="b9ccd-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b9ccd-156">NOTES</span></span>

## <span data-ttu-id="b9ccd-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9ccd-157">RELATED LINKS</span></span>
