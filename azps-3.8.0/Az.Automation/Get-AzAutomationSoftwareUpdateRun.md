---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d93820d12a2f61714c58341f835bef8cba832b84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074995"
---
# <span data-ttu-id="060cf-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="060cf-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="060cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="060cf-102">SYNOPSIS</span></span>
<span data-ttu-id="060cf-103">Получает список запущенных обновлений программного обеспечения службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="060cf-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="060cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="060cf-104">SYNTAX</span></span>

### <span data-ttu-id="060cf-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="060cf-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="060cf-106">ById</span><span class="sxs-lookup"><span data-stu-id="060cf-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="060cf-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="060cf-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="060cf-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="060cf-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="060cf-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="060cf-109">DESCRIPTION</span></span>
<span data-ttu-id="060cf-110">Командлет Get-AzAutomationSoftwareUpdateRun возвращает список запущенных обновлений программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="060cf-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="060cf-111">Так как конфигурация обновления программного обеспечения имеет связанное расписание, ее можно запускать несколько повременных событий.</span><span class="sxs-lookup"><span data-stu-id="060cf-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="060cf-112">Каждый раз, когда запускается расписание, будет создан прогон обновления.</span><span class="sxs-lookup"><span data-stu-id="060cf-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="060cf-113">Прогон обновления — это совокупность результатов всех запущенных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="060cf-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="060cf-114">Вы можете получить доступ к определенной конфигурации обновления программного обеспечения, передав параметр SoftwareUpdateConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="060cf-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="060cf-115">Для получения конкретных запусков необходимо передать параметр Name.</span><span class="sxs-lookup"><span data-stu-id="060cf-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="060cf-116">Вы также можете выдавать список запусков с определенным состоянием, запускать определенную операционную систему или запускать ее по истечении определенного времени, передавая соответствующий параметр.</span><span class="sxs-lookup"><span data-stu-id="060cf-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="060cf-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="060cf-117">EXAMPLES</span></span>

### <span data-ttu-id="060cf-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="060cf-118">Example 1</span></span>
<span data-ttu-id="060cf-119">В этом примере перечислены все запуски обновлений, инициированные определенной конфигурацией обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="060cf-119">This example list all update runs triggered by a specific software update configuration.</span></span>

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

## <span data-ttu-id="060cf-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="060cf-120">PARAMETERS</span></span>

### <span data-ttu-id="060cf-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="060cf-121">-AutomationAccountName</span></span>
<span data-ttu-id="060cf-122">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="060cf-122">The automation account name.</span></span>

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

### <span data-ttu-id="060cf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="060cf-123">-DefaultProfile</span></span>
<span data-ttu-id="060cf-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="060cf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="060cf-125">-ID</span><span class="sxs-lookup"><span data-stu-id="060cf-125">-Id</span></span>
<span data-ttu-id="060cf-126">Идентификатор запуска конфигурации обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="060cf-126">Id of the software update configuration run.</span></span>

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

### <span data-ttu-id="060cf-127">-Для заданной операционной</span><span class="sxs-lookup"><span data-stu-id="060cf-127">-OperatingSystem</span></span>
<span data-ttu-id="060cf-128">Операционная система для запуска.</span><span class="sxs-lookup"><span data-stu-id="060cf-128">The operating system of the run.</span></span>

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

### <span data-ttu-id="060cf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="060cf-129">-ResourceGroupName</span></span>
<span data-ttu-id="060cf-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="060cf-130">The resource group name.</span></span>

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

### <span data-ttu-id="060cf-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="060cf-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="060cf-132">Конфигурация обновления программного обеспечения активировала запуск.</span><span class="sxs-lookup"><span data-stu-id="060cf-132">The software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="060cf-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="060cf-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="060cf-134">Имя конфигурации обновления программного обеспечения, вызвавшего запуск.</span><span class="sxs-lookup"><span data-stu-id="060cf-134">Name of the software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="060cf-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="060cf-135">-StartTime</span></span>
<span data-ttu-id="060cf-136">Минимальное время начала выполнения.</span><span class="sxs-lookup"><span data-stu-id="060cf-136">Minimum start time of the run.</span></span>

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

### <span data-ttu-id="060cf-137">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="060cf-137">-Status</span></span>
<span data-ttu-id="060cf-138">Состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="060cf-138">Status of the run.</span></span>

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

### <span data-ttu-id="060cf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="060cf-139">CommonParameters</span></span>
<span data-ttu-id="060cf-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="060cf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="060cf-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="060cf-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="060cf-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="060cf-142">INPUTS</span></span>

### <span data-ttu-id="060cf-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="060cf-143">System.Guid</span></span>

### <span data-ttu-id="060cf-144">System. String</span><span class="sxs-lookup"><span data-stu-id="060cf-144">System.String</span></span>

### <span data-ttu-id="060cf-145">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="060cf-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="060cf-146">System. Nullable "1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. OperatingSystemType, Microsoft. Azure. командлеты = нейтральный, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="060cf-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="060cf-147">System. Nullable "1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRunStatus, Microsoft. Azure. командлеты = нейтральный, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="060cf-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="060cf-148">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="060cf-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="060cf-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="060cf-149">OUTPUTS</span></span>

### <span data-ttu-id="060cf-150">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="060cf-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="060cf-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="060cf-151">NOTES</span></span>

## <span data-ttu-id="060cf-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="060cf-152">RELATED LINKS</span></span>
