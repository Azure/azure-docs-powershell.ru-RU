---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: 49c8693984dc695f3d47b8066228cf2f82d5b267
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014168"
---
# <span data-ttu-id="4bb46-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="4bb46-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="4bb46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bb46-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb46-103">Список обновлений программного обеспечения автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb46-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="4bb46-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4bb46-104">SYNTAX</span></span>

### <span data-ttu-id="4bb46-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4bb46-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bb46-106">ById</span><span class="sxs-lookup"><span data-stu-id="4bb46-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bb46-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="4bb46-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4bb46-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="4bb46-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4bb46-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bb46-109">DESCRIPTION</span></span>
<span data-ttu-id="4bb46-110">Этот Get-AzAutomationSoftwareUpdateRun возвращает список запусков обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="4bb46-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="4bb46-111">Так как у конфигурации обновления программного обеспечения есть связанное расписание, его можно запускать несколько раз.</span><span class="sxs-lookup"><span data-stu-id="4bb46-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="4bb46-112">При каждом запуске расписания создается обновление.</span><span class="sxs-lookup"><span data-stu-id="4bb46-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="4bb46-113">Запуск обновления — это агрегат результатов всех запусков компьютера.</span><span class="sxs-lookup"><span data-stu-id="4bb46-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="4bb46-114">Вы можете получить запуск для определенной конфигурации обновления программного обеспечения, передавая параметр SoftwareUpdateConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="4bb46-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="4bb46-115">Чтобы получить определенные запускы, необходимо пройти параметр имени.</span><span class="sxs-lookup"><span data-stu-id="4bb46-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="4bb46-116">Вы также можете перечислить запуск с определенным состоянием, целевую работу с определенной операционной системой или запуск после определенного времени путем передачи соответствующего параметра.</span><span class="sxs-lookup"><span data-stu-id="4bb46-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="4bb46-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4bb46-117">EXAMPLES</span></span>

### <span data-ttu-id="4bb46-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4bb46-118">Example 1</span></span>
<span data-ttu-id="4bb46-119">В этом примере все обновления запускаются с помощью определенной конфигурации обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="4bb46-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
                                               -AutomationAccountName "myaccount" `
                                               -SoftwareUpdateConfigurationName "MyUpdateConfiguration"

RunId                           : ec9ce57f-da18-44be-b33b-651a0f93cb52
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 11:37:42 PM +00:00
EndTime                         : 5/22/2018 11:38:31 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ec9ce57f-da18-44be-b33b-651a0f93cb52
CreationTime                    : 5/22/2018 11:37:42 PM +00:00
LastModifiedTime                : 5/22/2018 11:38:54 PM +00:00
Description                     :

RunId                           : ac9396c7-a837-43d4-be97-fbfe46c80baa
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 10:00:47 PM +00:00
EndTime                         : 5/22/2018 10:02:20 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ac9396c7-a837-43d4-be97-fbfe46c80baa
CreationTime                    : 5/22/2018 10:00:47 PM +00:00
LastModifiedTime                : 5/22/2018 10:02:58 PM +00:00
```

## <span data-ttu-id="4bb46-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bb46-120">PARAMETERS</span></span>

### <span data-ttu-id="4bb46-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4bb46-121">-AutomationAccountName</span></span>
<span data-ttu-id="4bb46-122">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4bb46-122">The automation account name.</span></span>

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

### <span data-ttu-id="4bb46-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb46-123">-DefaultProfile</span></span>
<span data-ttu-id="4bb46-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb46-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bb46-125">-Id</span><span class="sxs-lookup"><span data-stu-id="4bb46-125">-Id</span></span>
<span data-ttu-id="4bb46-126">Ид конфигурации обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="4bb46-126">Id of the software update configuration run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb46-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="4bb46-127">-OperatingSystem</span></span>
<span data-ttu-id="4bb46-128">Операционная система запуска.</span><span class="sxs-lookup"><span data-stu-id="4bb46-128">The operating system of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb46-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bb46-129">-ResourceGroupName</span></span>
<span data-ttu-id="4bb46-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4bb46-130">The resource group name.</span></span>

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

### <span data-ttu-id="4bb46-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bb46-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="4bb46-132">Запуск запуска вызван конфигурацией обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="4bb46-132">The software update configuration triggered the run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb46-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="4bb46-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="4bb46-134">Имя конфигурации обновления программного обеспечения, активировали запуск.</span><span class="sxs-lookup"><span data-stu-id="4bb46-134">Name of the software update configuration triggered the run.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb46-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4bb46-135">-StartTime</span></span>
<span data-ttu-id="4bb46-136">Минимальное время начала запуска.</span><span class="sxs-lookup"><span data-stu-id="4bb46-136">Minimum start time of the run.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByAll, BySucName, BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb46-137">-Status</span><span class="sxs-lookup"><span data-stu-id="4bb46-137">-Status</span></span>
<span data-ttu-id="4bb46-138">Состояние запуска.</span><span class="sxs-lookup"><span data-stu-id="4bb46-138">Status of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb46-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb46-139">CommonParameters</span></span>
<span data-ttu-id="4bb46-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bb46-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb46-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bb46-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb46-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4bb46-142">INPUTS</span></span>

### <span data-ttu-id="4bb46-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4bb46-143">System.Guid</span></span>

### <span data-ttu-id="4bb46-144">System.String</span><span class="sxs-lookup"><span data-stu-id="4bb46-144">System.String</span></span>

### <span data-ttu-id="4bb46-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bb46-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="4bb46-146">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4bb46-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4bb46-147">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4bb46-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4bb46-148">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4bb46-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="4bb46-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4bb46-149">OUTPUTS</span></span>

### <span data-ttu-id="4bb46-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="4bb46-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="4bb46-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4bb46-151">NOTES</span></span>

## <span data-ttu-id="4bb46-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bb46-152">RELATED LINKS</span></span>
