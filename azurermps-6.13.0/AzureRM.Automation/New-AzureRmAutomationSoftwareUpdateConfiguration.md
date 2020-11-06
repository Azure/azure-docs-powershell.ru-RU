---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f66d22e8ca07812ab76c482c29018f2a639d84f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565953"
---
# <span data-ttu-id="efc35-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="efc35-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="efc35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="efc35-102">SYNOPSIS</span></span>
<span data-ttu-id="efc35-103">Создает запланированную конфигурацию обновления программного обеспечения службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="efc35-103">Creates a scheduled azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efc35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="efc35-104">SYNTAX</span></span>

### <span data-ttu-id="efc35-105">Windows (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="efc35-105">Windows (Default)</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows]
 [-AzureVMResourceId <String[]>] [-NonAzureComputer <String[]>] [-Duration <TimeSpan>]
 [-IncludedUpdateClassification <WindowsUpdateClasses[]>] [-ExcludedKbNumber <String[]>]
 [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efc35-106">Linux</span><span class="sxs-lookup"><span data-stu-id="efc35-106">Linux</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-AzureVMResourceId <String[]>]
 [-NonAzureComputer <String[]>] [-Duration <TimeSpan>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efc35-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="efc35-107">DESCRIPTION</span></span>
<span data-ttu-id="efc35-108">Создание конфигурации обновления программного обеспечения, которая запускается по расписанию для обновления списка компьютеров.</span><span class="sxs-lookup"><span data-stu-id="efc35-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="efc35-109">Компьютеры включают как виртуальные машины Azure, так и компьютеры без Azure.</span><span class="sxs-lookup"><span data-stu-id="efc35-109">Computers include both azure virtual machines or non-azure computers.</span></span>

## <span data-ttu-id="efc35-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="efc35-110">EXAMPLES</span></span>

### <span data-ttu-id="efc35-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="efc35-111">Example 1</span></span>
<span data-ttu-id="efc35-112">Создание конфигурации обновления программного обеспечения для установки критических обновлений на двух виртуальных машинах Windows Azure каждый раз в субботу 9PM.</span><span class="sxs-lookup"><span data-stu-id="efc35-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="efc35-113">В этом примере длительность обновления задается в 2 часа.</span><span class="sxs-lookup"><span data-stu-id="efc35-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzureRmAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceIds $targetMachines `
                                                 -IncludedUpdateClassifications Critical `
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

## <span data-ttu-id="efc35-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="efc35-114">PARAMETERS</span></span>

### <span data-ttu-id="efc35-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="efc35-115">-AutomationAccountName</span></span>
<span data-ttu-id="efc35-116">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="efc35-116">The automation account name.</span></span>

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

### <span data-ttu-id="efc35-117">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="efc35-117">-AzureVMResourceId</span></span>
<span data-ttu-id="efc35-118">Идентификаторы ресурсов для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="efc35-118">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="efc35-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc35-119">-DefaultProfile</span></span>
<span data-ttu-id="efc35-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="efc35-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efc35-121">-Duration</span><span class="sxs-lookup"><span data-stu-id="efc35-121">-Duration</span></span>
<span data-ttu-id="efc35-122">Максимальная длительность обновления.</span><span class="sxs-lookup"><span data-stu-id="efc35-122">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="efc35-123">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="efc35-123">-ExcludedKbNumber</span></span>
<span data-ttu-id="efc35-124">KB количество исключенных обновлений.</span><span class="sxs-lookup"><span data-stu-id="efc35-124">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="efc35-125">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="efc35-125">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="efc35-126">Исключены маски пакетов Linux.</span><span class="sxs-lookup"><span data-stu-id="efc35-126">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="efc35-127">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="efc35-127">-IncludedKbNumber</span></span>
<span data-ttu-id="efc35-128">Число KB, включенных в набор обновлений.</span><span class="sxs-lookup"><span data-stu-id="efc35-128">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="efc35-129">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="efc35-129">-IncludedPackageClassification</span></span>
<span data-ttu-id="efc35-130">Включены классификации пакетов Linux.</span><span class="sxs-lookup"><span data-stu-id="efc35-130">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="efc35-131">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="efc35-131">-IncludedPackageNameMask</span></span>
<span data-ttu-id="efc35-132">Комплекты масок пакетов Linux.</span><span class="sxs-lookup"><span data-stu-id="efc35-132">Included Linux package masks.</span></span>

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

### <span data-ttu-id="efc35-133">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="efc35-133">-IncludedUpdateClassification</span></span>
<span data-ttu-id="efc35-134">Включены классификации обновлений Windows.</span><span class="sxs-lookup"><span data-stu-id="efc35-134">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="efc35-135">-Linux</span><span class="sxs-lookup"><span data-stu-id="efc35-135">-Linux</span></span>
<span data-ttu-id="efc35-136">Указывает на то, что конфигурация обновления программного обеспечения нацелена на компьютеры операционной системы Linux.</span><span class="sxs-lookup"><span data-stu-id="efc35-136">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="efc35-137">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="efc35-137">-NonAzureComputer</span></span>
<span data-ttu-id="efc35-138">Имена компьютеров, не являющихся Azure.</span><span class="sxs-lookup"><span data-stu-id="efc35-138">Non-Azure computer names.</span></span>

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

### <span data-ttu-id="efc35-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc35-139">-ResourceGroupName</span></span>
<span data-ttu-id="efc35-140">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="efc35-140">The resource group name.</span></span>

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

### <span data-ttu-id="efc35-141">-Планирование</span><span class="sxs-lookup"><span data-stu-id="efc35-141">-Schedule</span></span>
<span data-ttu-id="efc35-142">Объект Schedule, используемый для настройки обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="efc35-142">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="efc35-143">-Windows</span><span class="sxs-lookup"><span data-stu-id="efc35-143">-Windows</span></span>
<span data-ttu-id="efc35-144">Указывает на то, что конфигурация обновления программного обеспечения нацелена на компьютеры операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="efc35-144">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="efc35-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efc35-145">-Confirm</span></span>
<span data-ttu-id="efc35-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="efc35-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc35-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc35-147">-WhatIf</span></span>
<span data-ttu-id="efc35-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="efc35-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efc35-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="efc35-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc35-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc35-150">CommonParameters</span></span>
<span data-ttu-id="efc35-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="efc35-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc35-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc35-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc35-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="efc35-153">INPUTS</span></span>

### <span data-ttu-id="efc35-154">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="efc35-154">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="efc35-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="efc35-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="efc35-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="efc35-156">System.String[]</span></span>

### <span data-ttu-id="efc35-157">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="efc35-157">System.TimeSpan</span></span>

### <span data-ttu-id="efc35-158">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="efc35-158">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="efc35-159">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="efc35-159">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="efc35-160">System. String</span><span class="sxs-lookup"><span data-stu-id="efc35-160">System.String</span></span>

## <span data-ttu-id="efc35-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="efc35-161">OUTPUTS</span></span>

### <span data-ttu-id="efc35-162">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="efc35-162">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="efc35-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="efc35-163">NOTES</span></span>

## <span data-ttu-id="efc35-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="efc35-164">RELATED LINKS</span></span>
