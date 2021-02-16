---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d93820d12a2f61714c58341f835bef8cba832b84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235228"
---
# <span data-ttu-id="7b599-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="7b599-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="7b599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b599-102">SYNOPSIS</span></span>
<span data-ttu-id="7b599-103">Возвращает список обновлений программного обеспечения автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="7b599-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="7b599-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7b599-104">SYNTAX</span></span>

### <span data-ttu-id="7b599-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b599-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b599-106">ById</span><span class="sxs-lookup"><span data-stu-id="7b599-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b599-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="7b599-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b599-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="7b599-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b599-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b599-109">DESCRIPTION</span></span>
<span data-ttu-id="7b599-110">Новый Get-AzAutomationSoftwareUpdateRun возвращает список запусков обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="7b599-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="7b599-111">Так как у конфигурации обновления программного обеспечения есть связанное расписание, ее можно запускать несколько раз.</span><span class="sxs-lookup"><span data-stu-id="7b599-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="7b599-112">При каждом запуске расписания создается обновление.</span><span class="sxs-lookup"><span data-stu-id="7b599-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="7b599-113">Запуск обновления — это агрегат результатов всех запусков компьютера.</span><span class="sxs-lookup"><span data-stu-id="7b599-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="7b599-114">Вы можете получить запуск для определенной конфигурации обновления программного обеспечения, пройдя параметр SoftwareUpdateConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="7b599-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="7b599-115">Чтобы получить определенные запускы, необходимо пройти параметр имени.</span><span class="sxs-lookup"><span data-stu-id="7b599-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="7b599-116">Вы также можете перечислить запуск с определенным состоянием, целевую работу с определенной операционной системой или запуск после определенного времени путем передачи соответствующего параметра.</span><span class="sxs-lookup"><span data-stu-id="7b599-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="7b599-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7b599-117">EXAMPLES</span></span>

### <span data-ttu-id="7b599-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7b599-118">Example 1</span></span>
<span data-ttu-id="7b599-119">В этом примере все обновления запускаются с помощью определенной конфигурации обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="7b599-119">This example list all update runs triggered by a specific software update configuration.</span></span>

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

## <span data-ttu-id="7b599-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b599-120">PARAMETERS</span></span>

### <span data-ttu-id="7b599-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7b599-121">-AutomationAccountName</span></span>
<span data-ttu-id="7b599-122">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7b599-122">The automation account name.</span></span>

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

### <span data-ttu-id="7b599-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b599-123">-DefaultProfile</span></span>
<span data-ttu-id="7b599-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b599-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b599-125">-Id</span><span class="sxs-lookup"><span data-stu-id="7b599-125">-Id</span></span>
<span data-ttu-id="7b599-126">Ид конфигурации обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="7b599-126">Id of the software update configuration run.</span></span>

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

### <span data-ttu-id="7b599-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="7b599-127">-OperatingSystem</span></span>
<span data-ttu-id="7b599-128">Операционная система запуска.</span><span class="sxs-lookup"><span data-stu-id="7b599-128">The operating system of the run.</span></span>

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

### <span data-ttu-id="7b599-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b599-129">-ResourceGroupName</span></span>
<span data-ttu-id="7b599-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b599-130">The resource group name.</span></span>

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

### <span data-ttu-id="7b599-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b599-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="7b599-132">Запуск запуска вызван конфигурацией обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="7b599-132">The software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="7b599-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7b599-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="7b599-134">Имя конфигурации обновления программного обеспечения, активировали запуск.</span><span class="sxs-lookup"><span data-stu-id="7b599-134">Name of the software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="7b599-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7b599-135">-StartTime</span></span>
<span data-ttu-id="7b599-136">Минимальное время начала запуска.</span><span class="sxs-lookup"><span data-stu-id="7b599-136">Minimum start time of the run.</span></span>

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

### <span data-ttu-id="7b599-137">-Status</span><span class="sxs-lookup"><span data-stu-id="7b599-137">-Status</span></span>
<span data-ttu-id="7b599-138">Состояние запуска.</span><span class="sxs-lookup"><span data-stu-id="7b599-138">Status of the run.</span></span>

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

### <span data-ttu-id="7b599-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b599-139">CommonParameters</span></span>
<span data-ttu-id="7b599-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b599-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b599-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b599-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b599-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b599-142">INPUTS</span></span>

### <span data-ttu-id="7b599-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7b599-143">System.Guid</span></span>

### <span data-ttu-id="7b599-144">System.String</span><span class="sxs-lookup"><span data-stu-id="7b599-144">System.String</span></span>

### <span data-ttu-id="7b599-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b599-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="7b599-146">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="7b599-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7b599-147">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="7b599-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7b599-148">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7b599-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="7b599-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7b599-149">OUTPUTS</span></span>

### <span data-ttu-id="7b599-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="7b599-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="7b599-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7b599-151">NOTES</span></span>

## <span data-ttu-id="7b599-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b599-152">RELATED LINKS</span></span>
