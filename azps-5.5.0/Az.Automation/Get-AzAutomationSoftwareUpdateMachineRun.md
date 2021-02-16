---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 19c0321b1c915519b7c3617b52810da18e534521
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233692"
---
# <span data-ttu-id="e8b91-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="e8b91-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="e8b91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8b91-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b91-103">Возвращает список, на который ведется компьютер конфигурации обновления программного обеспечения автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="e8b91-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="e8b91-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e8b91-104">SYNTAX</span></span>

### <span data-ttu-id="e8b91-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8b91-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e8b91-106">ById</span><span class="sxs-lookup"><span data-stu-id="e8b91-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8b91-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="e8b91-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8b91-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="e8b91-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8b91-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8b91-109">DESCRIPTION</span></span>
<span data-ttu-id="e8b91-110">Этот cmdlet возвращает список запусков компьютера.</span><span class="sxs-lookup"><span data-stu-id="e8b91-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="e8b91-111">При каждом запуске обновления программного обеспечения запускается компьютер для каждого конечного компьютера, на который будет вести настройка обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="e8b91-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="e8b91-112">Чтобы запустить определенный компьютер, передите параметр ID.</span><span class="sxs-lookup"><span data-stu-id="e8b91-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="e8b91-113">Вы можете перечислить все запускы компьютера, все запускы для определенного компьютера и все запускы с определенным состоянием, указав соответствующие параметры.</span><span class="sxs-lookup"><span data-stu-id="e8b91-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="e8b91-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e8b91-114">EXAMPLES</span></span>

### <span data-ttu-id="e8b91-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8b91-115">Example 1</span></span>
<span data-ttu-id="e8b91-116">В этом примере возвращаются все сбойные компьютеры для указанной виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="e8b91-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


```powershell
PS C:\> $targetComputer = "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm"
PS C:\> Get-AzAutomationSoftwareUpdateMachineRun -ResourceGroupName "mygroup" `
                                                      -AutomationAccountName "myaccount" `
                                                      -TargetComputer $targetComputer `
                                                      -Status Failed

MachineRunId          : 0033d6d6-828d-4712-adab-293cc4fc8809
TargetComputer        : /subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm
TargetComputerType    : AzureVirtualMachines
SoftwareUpdateRunId   : 46568d26-0182-49b2-8bfd-af3455780397
OperatingSystem       : Windows
Status                : Failed
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : 0033d6d6-828d-4712-adab-293cc4fc8809
CreationTime          : 5/17/2018 2:06:44 AM +00:00
LastModifiedTime      : 5/17/2018 2:08:49 AM +00:00
```

## <span data-ttu-id="e8b91-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8b91-117">PARAMETERS</span></span>

### <span data-ttu-id="e8b91-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e8b91-118">-AutomationAccountName</span></span>
<span data-ttu-id="e8b91-119">Имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="e8b91-119">The automation account name.</span></span>

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

### <span data-ttu-id="e8b91-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b91-120">-DefaultProfile</span></span>
<span data-ttu-id="e8b91-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8b91-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8b91-122">-Id</span><span class="sxs-lookup"><span data-stu-id="e8b91-122">-Id</span></span>
<span data-ttu-id="e8b91-123">ИД запуска компьютера обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="e8b91-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="e8b91-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8b91-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8b91-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e8b91-125">The resource group name.</span></span>

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

### <span data-ttu-id="e8b91-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="e8b91-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="e8b91-127">Запустится обновление программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="e8b91-127">The software update run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun
Parameter Sets: BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b91-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="e8b91-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="e8b91-129">ИД запуска обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="e8b91-129">Id of the software update run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: BySucrId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b91-130">-Status</span><span class="sxs-lookup"><span data-stu-id="e8b91-130">-Status</span></span>
<span data-ttu-id="e8b91-131">Состояние запуска компьютера.</span><span class="sxs-lookup"><span data-stu-id="e8b91-131">Status of the machine run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus]
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded, FailedToStart

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b91-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="e8b91-132">-TargetComputer</span></span>
<span data-ttu-id="e8b91-133">на целевом компьютере для запуска компьютера.</span><span class="sxs-lookup"><span data-stu-id="e8b91-133">target computer for the machine run.</span></span>
<span data-ttu-id="e8b91-134">Может быть либо именем компьютера, которое не является az, либо именем ресурса azure VM.</span><span class="sxs-lookup"><span data-stu-id="e8b91-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b91-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b91-135">CommonParameters</span></span>
<span data-ttu-id="e8b91-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8b91-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b91-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8b91-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b91-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e8b91-138">INPUTS</span></span>

### <span data-ttu-id="e8b91-139">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e8b91-139">System.Guid</span></span>

### <span data-ttu-id="e8b91-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="e8b91-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="e8b91-141">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e8b91-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e8b91-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e8b91-142">System.String</span></span>

## <span data-ttu-id="e8b91-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e8b91-143">OUTPUTS</span></span>

### <span data-ttu-id="e8b91-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="e8b91-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="e8b91-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e8b91-145">NOTES</span></span>

## <span data-ttu-id="e8b91-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8b91-146">RELATED LINKS</span></span>
