---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d49d99f8edd3ffe0c25886447eac0bbd15837fc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733487"
---
# <span data-ttu-id="bb6d5-101">Get-AzureRmAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="bb6d5-101">Get-AzureRmAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="bb6d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb6d5-102">SYNOPSIS</span></span>
<span data-ttu-id="bb6d5-103">Получает список запущенных обновлений программного обеспечения службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-103">Gets a list of azure automation software update runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb6d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb6d5-104">SYNTAX</span></span>

### <span data-ttu-id="bb6d5-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb6d5-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>]
 [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb6d5-106">ById</span><span class="sxs-lookup"><span data-stu-id="bb6d5-106">ById</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb6d5-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="bb6d5-107">BySucName</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb6d5-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="bb6d5-108">BySuc</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb6d5-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb6d5-109">DESCRIPTION</span></span>
<span data-ttu-id="bb6d5-110">Командлет Get-AzureRmAutomationSoftwareUpdateRun возвращает список запущенных обновлений программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-110">The Get-AzureRmAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="bb6d5-111">Так как конфигурация обновления программного обеспечения имеет связанное расписание, ее можно запускать несколько повременных событий.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="bb6d5-112">Каждый раз, когда запускается расписание, будет создан прогон обновления.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="bb6d5-113">Прогон обновления — это совокупность результатов всех запущенных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="bb6d5-114">Вы можете получить доступ к определенной конфигурации обновления программного обеспечения, передав параметр SoftwareUpdateConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="bb6d5-115">Для получения конкретных запусков необходимо передать параметр Name.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="bb6d5-116">Вы также можете выдавать список запусков с определенным состоянием, запускать определенную систему operatins или запускать ее по истечении определенного времени, передавая соответствующий параметр.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-116">You can also list runs with specific status, runs targeting specific operatins system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="bb6d5-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb6d5-117">EXAMPLES</span></span>

### <span data-ttu-id="bb6d5-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bb6d5-118">Example 1</span></span>
<span data-ttu-id="bb6d5-119">В этом примере перечислены все запуски обновлений, инициированные определенной конфигурацией обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
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

## <span data-ttu-id="bb6d5-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb6d5-120">PARAMETERS</span></span>

### <span data-ttu-id="bb6d5-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bb6d5-121">-AutomationAccountName</span></span>
<span data-ttu-id="bb6d5-122">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-122">The automation account name.</span></span>

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

### <span data-ttu-id="bb6d5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb6d5-123">-DefaultProfile</span></span>
<span data-ttu-id="bb6d5-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb6d5-125">-ID</span><span class="sxs-lookup"><span data-stu-id="bb6d5-125">-Id</span></span>
<span data-ttu-id="bb6d5-126">Идентификатор запуска конфигурации обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-126">Id of the software update configuration run.</span></span>

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

### <span data-ttu-id="bb6d5-127">-Для заданной операционной</span><span class="sxs-lookup"><span data-stu-id="bb6d5-127">-OperatingSystem</span></span>
<span data-ttu-id="bb6d5-128">Операционная система для запуска.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-128">The operating system of the run.</span></span>

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

### <span data-ttu-id="bb6d5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb6d5-129">-ResourceGroupName</span></span>
<span data-ttu-id="bb6d5-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-130">The resource group name.</span></span>

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

### <span data-ttu-id="bb6d5-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb6d5-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="bb6d5-132">Конфигурация обновления программного обеспечения активировала запуск.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-132">The software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="bb6d5-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="bb6d5-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="bb6d5-134">Имя конфигурации обновления программного обеспечения, вызвавшего запуск.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-134">Name of the software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="bb6d5-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bb6d5-135">-StartTime</span></span>
<span data-ttu-id="bb6d5-136">Минимальное время начала выполнения.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-136">Minimum start time of the run.</span></span>

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

### <span data-ttu-id="bb6d5-137">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="bb6d5-137">-Status</span></span>
<span data-ttu-id="bb6d5-138">Состояние выполнения.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-138">Status of the run.</span></span>

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

### <span data-ttu-id="bb6d5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb6d5-139">CommonParameters</span></span>
<span data-ttu-id="bb6d5-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb6d5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb6d5-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb6d5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb6d5-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb6d5-142">INPUTS</span></span>

### <span data-ttu-id="bb6d5-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="bb6d5-143">System.Guid</span></span>

### <span data-ttu-id="bb6d5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="bb6d5-144">System.String</span></span>

### <span data-ttu-id="bb6d5-145">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb6d5-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="bb6d5-146">System. Nullable "1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. OperatingSystemType, Microsoft. Azure. Commands. ResourceManager. Automation, версия = 5.1.1.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="bb6d5-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.Commands.ResourceManager.Automation, Version=5.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="bb6d5-147">System. Nullable "1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRunStatus, Microsoft. Azure. Commands. ResourceManager. Automation, версия = 5.1.1.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="bb6d5-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.Commands.ResourceManager.Automation, Version=5.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="bb6d5-148">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bb6d5-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="bb6d5-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb6d5-149">OUTPUTS</span></span>

### <span data-ttu-id="bb6d5-150">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="bb6d5-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="bb6d5-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb6d5-151">NOTES</span></span>

## <span data-ttu-id="bb6d5-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb6d5-152">RELATED LINKS</span></span>
