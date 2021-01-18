---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: d54acf3ad4e47c173b8ec4ef2fd37145c6dbf198
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509966"
---
# <span data-ttu-id="de34b-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="de34b-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="de34b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de34b-102">SYNOPSIS</span></span>
<span data-ttu-id="de34b-103">Создает запланированную конфигурацию обновления программного обеспечения автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="de34b-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="de34b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="de34b-104">SYNTAX</span></span>

### <span data-ttu-id="de34b-105">Windows (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="de34b-105">Windows (Default)</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedUpdateClassification <WindowsUpdateClasses[]>]
 [-ExcludedKbNumber <String[]>] [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de34b-106">Linux</span><span class="sxs-lookup"><span data-stu-id="de34b-106">Linux</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de34b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de34b-107">DESCRIPTION</span></span>
<span data-ttu-id="de34b-108">Создает конфигурацию обновления программного обеспечения, которая выполняется по расписанию для обновления списка компьютеров.</span><span class="sxs-lookup"><span data-stu-id="de34b-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="de34b-109">Компьютеры включают как виртуальные машины Azure, так и компьютеры, не включаочные в az.</span><span class="sxs-lookup"><span data-stu-id="de34b-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="de34b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="de34b-110">EXAMPLES</span></span>

### <span data-ttu-id="de34b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="de34b-111">Example 1</span></span>
<span data-ttu-id="de34b-112">Создает конфигурацию обновления программного обеспечения для установки критических обновлений на двух виртуальных машинах Windows Azure каждую субботу в 9:00.</span><span class="sxs-lookup"><span data-stu-id="de34b-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="de34b-113">В этом примере для длительности обновления установлено 2 часа.</span><span class="sxs-lookup"><span data-stu-id="de34b-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceId $targetMachines `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :
```

## <span data-ttu-id="de34b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de34b-114">PARAMETERS</span></span>

### <span data-ttu-id="de34b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="de34b-115">-AutomationAccountName</span></span>
<span data-ttu-id="de34b-116">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="de34b-116">The automation account name.</span></span>

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

### <span data-ttu-id="de34b-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="de34b-117">-AzureQuery</span></span>
<span data-ttu-id="de34b-118">Динамический групповой запрос azure.</span><span class="sxs-lookup"><span data-stu-id="de34b-118">Dynamic group azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="de34b-119">-AzureVMResourceId</span></span>
<span data-ttu-id="de34b-120">ИД ресурсов для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="de34b-120">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de34b-121">-DefaultProfile</span></span>
<span data-ttu-id="de34b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de34b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-123">-Duration</span><span class="sxs-lookup"><span data-stu-id="de34b-123">-Duration</span></span>
<span data-ttu-id="de34b-124">Максимальная длительность обновления.</span><span class="sxs-lookup"><span data-stu-id="de34b-124">Maximum duration for the update.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="de34b-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="de34b-126">KB-номера исключенных обновлений.</span><span class="sxs-lookup"><span data-stu-id="de34b-126">KB numbers of excluded updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="de34b-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="de34b-128">Исключение масок пакетов Linux.</span><span class="sxs-lookup"><span data-stu-id="de34b-128">Excluded Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="de34b-129">-IncludedKbNumber</span></span>
<span data-ttu-id="de34b-130">KB-номера включенных обновлений.</span><span class="sxs-lookup"><span data-stu-id="de34b-130">KB numbers of included updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="de34b-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="de34b-132">Классификации пакетов Linux.</span><span class="sxs-lookup"><span data-stu-id="de34b-132">Included Linux package classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]
Parameter Sets: Linux
Aliases:
Accepted values: Unclassified, Critical, Security, Other

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="de34b-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="de34b-134">Входит в состав масок пакетов Linux.</span><span class="sxs-lookup"><span data-stu-id="de34b-134">Included Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="de34b-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="de34b-136">Классификации, включенные в Обновление Windows.</span><span class="sxs-lookup"><span data-stu-id="de34b-136">Included Windows Update classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]
Parameter Sets: Windows
Aliases:
Accepted values: Unclassified, Critical, Security, UpdateRollup, FeaturePack, ServicePack, Definition, Tools, Updates

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="de34b-137">-Linux</span></span>
<span data-ttu-id="de34b-138">Указывает на то, что конфигурация обновления программного обеспечения ориентирована на компьютеры с операционной системой Linux.</span><span class="sxs-lookup"><span data-stu-id="de34b-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="de34b-139">-NonAzureComputer</span></span>
<span data-ttu-id="de34b-140">Имена компьютеров не из Az.</span><span class="sxs-lookup"><span data-stu-id="de34b-140">Non-Az computer names.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="de34b-141">-NonAzureQuery</span></span>
<span data-ttu-id="de34b-142">Динамическая группа без запроса Azure.</span><span class="sxs-lookup"><span data-stu-id="de34b-142">Dynamic group non Azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.NonAzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="de34b-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="de34b-144">Опубликовать задачу.</span><span class="sxs-lookup"><span data-stu-id="de34b-144">Post task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="de34b-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="de34b-146">Параметр "Опубликовать задачу".</span><span class="sxs-lookup"><span data-stu-id="de34b-146">Post task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="de34b-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="de34b-148">Предварительная задача.</span><span class="sxs-lookup"><span data-stu-id="de34b-148">Pre task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="de34b-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="de34b-150">Параметр "Предварительная задача".</span><span class="sxs-lookup"><span data-stu-id="de34b-150">Pre task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="de34b-151">-RebootOnly</span></span>
<span data-ttu-id="de34b-152">Указывает на то, что конфигурация обновления программного обеспечения будет перезагружать только компьютеры.</span><span class="sxs-lookup"><span data-stu-id="de34b-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="de34b-153">-RebootSetting</span></span>
<span data-ttu-id="de34b-154">"Параметр перезагрузки".</span><span class="sxs-lookup"><span data-stu-id="de34b-154">Reboot Setting.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.RebootSetting
Parameter Sets: (All)
Aliases:
Accepted values: IfRequired, Never, Always, RebootOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de34b-155">-ResourceGroupName</span></span>
<span data-ttu-id="de34b-156">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="de34b-156">The resource group name.</span></span>

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

### <span data-ttu-id="de34b-157">-Расписание</span><span class="sxs-lookup"><span data-stu-id="de34b-157">-Schedule</span></span>
<span data-ttu-id="de34b-158">Объект "Расписание", используемый для настройки обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="de34b-158">Schedule object used for software update configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="de34b-159">-Windows</span></span>
<span data-ttu-id="de34b-160">Указывает на то, что конфигурация обновления программного обеспечения ориентирована на компьютеры операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="de34b-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de34b-161">-Confirm</span></span>
<span data-ttu-id="de34b-162">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de34b-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de34b-163">-WhatIf</span></span>
<span data-ttu-id="de34b-164">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de34b-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de34b-165">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="de34b-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de34b-166">CommonParameters</span></span>
<span data-ttu-id="de34b-167">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de34b-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de34b-168">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de34b-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de34b-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de34b-169">INPUTS</span></span>

### <span data-ttu-id="de34b-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="de34b-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="de34b-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="de34b-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="de34b-172">System.String[]</span><span class="sxs-lookup"><span data-stu-id="de34b-172">System.String[]</span></span>

### <span data-ttu-id="de34b-173">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="de34b-173">System.TimeSpan</span></span>

### <span data-ttu-id="de34b-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span><span class="sxs-lookup"><span data-stu-id="de34b-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="de34b-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span><span class="sxs-lookup"><span data-stu-id="de34b-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="de34b-176">System.String</span><span class="sxs-lookup"><span data-stu-id="de34b-176">System.String</span></span>

## <span data-ttu-id="de34b-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="de34b-177">OUTPUTS</span></span>

### <span data-ttu-id="de34b-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="de34b-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="de34b-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="de34b-179">NOTES</span></span>

## <span data-ttu-id="de34b-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de34b-180">RELATED LINKS</span></span>
