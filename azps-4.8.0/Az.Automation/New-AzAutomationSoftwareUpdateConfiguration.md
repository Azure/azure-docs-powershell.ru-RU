---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: d54acf3ad4e47c173b8ec4ef2fd37145c6dbf198
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077926"
---
# <span data-ttu-id="3712a-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="3712a-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="3712a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3712a-102">SYNOPSIS</span></span>
<span data-ttu-id="3712a-103">Создает запланированную конфигурацию обновления программного обеспечения службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="3712a-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="3712a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3712a-104">SYNTAX</span></span>

### <span data-ttu-id="3712a-105">Windows (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3712a-105">Windows (Default)</span></span>
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

### <span data-ttu-id="3712a-106">Linux</span><span class="sxs-lookup"><span data-stu-id="3712a-106">Linux</span></span>
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

## <span data-ttu-id="3712a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3712a-107">DESCRIPTION</span></span>
<span data-ttu-id="3712a-108">Создание конфигурации обновления программного обеспечения, которая запускается по расписанию для обновления списка компьютеров.</span><span class="sxs-lookup"><span data-stu-id="3712a-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="3712a-109">Компьютеры включают как виртуальные машины Azure, так и компьютеры без AZ.</span><span class="sxs-lookup"><span data-stu-id="3712a-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="3712a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3712a-110">EXAMPLES</span></span>

### <span data-ttu-id="3712a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3712a-111">Example 1</span></span>
<span data-ttu-id="3712a-112">Создание конфигурации обновления программного обеспечения для установки критических обновлений на двух виртуальных машинах Windows Azure каждый раз в субботу 9PM.</span><span class="sxs-lookup"><span data-stu-id="3712a-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="3712a-113">В этом примере длительность обновления задается в 2 часа.</span><span class="sxs-lookup"><span data-stu-id="3712a-113">Update duration is set to 2 hours in this example.</span></span>

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

## <span data-ttu-id="3712a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3712a-114">PARAMETERS</span></span>

### <span data-ttu-id="3712a-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3712a-115">-AutomationAccountName</span></span>
<span data-ttu-id="3712a-116">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3712a-116">The automation account name.</span></span>

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

### <span data-ttu-id="3712a-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="3712a-117">-AzureQuery</span></span>
<span data-ttu-id="3712a-118">Запрос на динамическую группу Azure.</span><span class="sxs-lookup"><span data-stu-id="3712a-118">Dynamic group azure query.</span></span>

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

### <span data-ttu-id="3712a-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="3712a-119">-AzureVMResourceId</span></span>
<span data-ttu-id="3712a-120">Идентификаторы ресурсов для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="3712a-120">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="3712a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3712a-121">-DefaultProfile</span></span>
<span data-ttu-id="3712a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3712a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3712a-123">-Duration</span><span class="sxs-lookup"><span data-stu-id="3712a-123">-Duration</span></span>
<span data-ttu-id="3712a-124">Максимальная длительность обновления.</span><span class="sxs-lookup"><span data-stu-id="3712a-124">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="3712a-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="3712a-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="3712a-126">KB количество исключенных обновлений.</span><span class="sxs-lookup"><span data-stu-id="3712a-126">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="3712a-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="3712a-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="3712a-128">Исключены маски пакетов Linux.</span><span class="sxs-lookup"><span data-stu-id="3712a-128">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="3712a-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="3712a-129">-IncludedKbNumber</span></span>
<span data-ttu-id="3712a-130">Число KB, включенных в набор обновлений.</span><span class="sxs-lookup"><span data-stu-id="3712a-130">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="3712a-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="3712a-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="3712a-132">Включены классификации пакетов Linux.</span><span class="sxs-lookup"><span data-stu-id="3712a-132">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="3712a-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="3712a-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="3712a-134">Комплекты масок пакетов Linux.</span><span class="sxs-lookup"><span data-stu-id="3712a-134">Included Linux package masks.</span></span>

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

### <span data-ttu-id="3712a-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="3712a-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="3712a-136">Включены классификации обновлений Windows.</span><span class="sxs-lookup"><span data-stu-id="3712a-136">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="3712a-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="3712a-137">-Linux</span></span>
<span data-ttu-id="3712a-138">Указывает на то, что конфигурация обновления программного обеспечения нацелена на компьютеры операционной системы Linux.</span><span class="sxs-lookup"><span data-stu-id="3712a-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="3712a-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="3712a-139">-NonAzureComputer</span></span>
<span data-ttu-id="3712a-140">Имена компьютеров без AZ.</span><span class="sxs-lookup"><span data-stu-id="3712a-140">Non-Az computer names.</span></span>

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

### <span data-ttu-id="3712a-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="3712a-141">-NonAzureQuery</span></span>
<span data-ttu-id="3712a-142">Динамическая группа: запрос не Azure.</span><span class="sxs-lookup"><span data-stu-id="3712a-142">Dynamic group non Azure query.</span></span>

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

### <span data-ttu-id="3712a-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="3712a-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="3712a-144">Опубликовать задачу.</span><span class="sxs-lookup"><span data-stu-id="3712a-144">Post task.</span></span>

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

### <span data-ttu-id="3712a-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="3712a-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="3712a-146">Параметр "опубликовать задачу".</span><span class="sxs-lookup"><span data-stu-id="3712a-146">Post task parameter.</span></span>

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

### <span data-ttu-id="3712a-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="3712a-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="3712a-148">Задача предустановлена.</span><span class="sxs-lookup"><span data-stu-id="3712a-148">Pre task.</span></span>

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

### <span data-ttu-id="3712a-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="3712a-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="3712a-150">Параметр предварительной задачи.</span><span class="sxs-lookup"><span data-stu-id="3712a-150">Pre task parameter.</span></span>

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

### <span data-ttu-id="3712a-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="3712a-151">-RebootOnly</span></span>
<span data-ttu-id="3712a-152">Указывает на то, что в конфигурации обновления программного обеспечения будут перезагружены только компьютеры.</span><span class="sxs-lookup"><span data-stu-id="3712a-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

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

### <span data-ttu-id="3712a-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="3712a-153">-RebootSetting</span></span>
<span data-ttu-id="3712a-154">Параметр перезагрузка.</span><span class="sxs-lookup"><span data-stu-id="3712a-154">Reboot Setting.</span></span>

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

### <span data-ttu-id="3712a-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3712a-155">-ResourceGroupName</span></span>
<span data-ttu-id="3712a-156">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3712a-156">The resource group name.</span></span>

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

### <span data-ttu-id="3712a-157">-Планирование</span><span class="sxs-lookup"><span data-stu-id="3712a-157">-Schedule</span></span>
<span data-ttu-id="3712a-158">Объект Schedule, используемый для настройки обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="3712a-158">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="3712a-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="3712a-159">-Windows</span></span>
<span data-ttu-id="3712a-160">Указывает на то, что конфигурация обновления программного обеспечения нацелена на компьютеры операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="3712a-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="3712a-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3712a-161">-Confirm</span></span>
<span data-ttu-id="3712a-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3712a-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3712a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3712a-163">-WhatIf</span></span>
<span data-ttu-id="3712a-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3712a-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3712a-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3712a-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3712a-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3712a-166">CommonParameters</span></span>
<span data-ttu-id="3712a-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3712a-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3712a-168">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3712a-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3712a-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3712a-169">INPUTS</span></span>

### <span data-ttu-id="3712a-170">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="3712a-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="3712a-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3712a-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3712a-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="3712a-172">System.String[]</span></span>

### <span data-ttu-id="3712a-173">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="3712a-173">System.TimeSpan</span></span>

### <span data-ttu-id="3712a-174">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="3712a-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="3712a-175">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="3712a-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="3712a-176">System. String</span><span class="sxs-lookup"><span data-stu-id="3712a-176">System.String</span></span>

## <span data-ttu-id="3712a-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3712a-177">OUTPUTS</span></span>

### <span data-ttu-id="3712a-178">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="3712a-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="3712a-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="3712a-179">NOTES</span></span>

## <span data-ttu-id="3712a-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3712a-180">RELATED LINKS</span></span>
