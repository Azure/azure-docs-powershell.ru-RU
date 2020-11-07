---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 80bba3309c0c23862fdb5efbbe6f373b8d1a964a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727827"
---
# <span data-ttu-id="114f4-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="114f4-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="114f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="114f4-102">SYNOPSIS</span></span>
<span data-ttu-id="114f4-103">Получает список запущенных компьютеров конфигурации обновлений программного обеспечения Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="114f4-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="114f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="114f4-104">SYNTAX</span></span>

### <span data-ttu-id="114f4-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="114f4-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="114f4-106">ById</span><span class="sxs-lookup"><span data-stu-id="114f4-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="114f4-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="114f4-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="114f4-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="114f4-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="114f4-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="114f4-109">DESCRIPTION</span></span>
<span data-ttu-id="114f4-110">Этот командлет возвращает список запущенных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="114f4-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="114f4-111">Каждый прогон обновления программного обеспечения инициирует запуск компьютера для каждого из целевых компьютеров конфигурации обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="114f4-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="114f4-112">Чтобы получить определенный запуск компьютера, передайте параметр ID.</span><span class="sxs-lookup"><span data-stu-id="114f4-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="114f4-113">Вы можете создать список всех запущенных компьютеров, все запущенные для определенного компьютера, все запускается с определенным состоянием, передавая соответствующие параметры.</span><span class="sxs-lookup"><span data-stu-id="114f4-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="114f4-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="114f4-114">EXAMPLES</span></span>

### <span data-ttu-id="114f4-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="114f4-115">Example 1</span></span>
<span data-ttu-id="114f4-116">В этом примере возвращается весь сбой компьютера, запущенный для указанной виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="114f4-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


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

## <span data-ttu-id="114f4-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="114f4-117">PARAMETERS</span></span>

### <span data-ttu-id="114f4-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="114f4-118">-AutomationAccountName</span></span>
<span data-ttu-id="114f4-119">Имя учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="114f4-119">The automation account name.</span></span>

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

### <span data-ttu-id="114f4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="114f4-120">-DefaultProfile</span></span>
<span data-ttu-id="114f4-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="114f4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="114f4-122">-ID</span><span class="sxs-lookup"><span data-stu-id="114f4-122">-Id</span></span>
<span data-ttu-id="114f4-123">Идентификационный номер компьютера, на котором выполняется обновление программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="114f4-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="114f4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="114f4-124">-ResourceGroupName</span></span>
<span data-ttu-id="114f4-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="114f4-125">The resource group name.</span></span>

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

### <span data-ttu-id="114f4-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="114f4-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="114f4-127">Запустится обновление программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="114f4-127">The software update run.</span></span>

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

### <span data-ttu-id="114f4-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="114f4-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="114f4-129">Код запуска обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="114f4-129">Id of the software update run.</span></span>

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

### <span data-ttu-id="114f4-130">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="114f4-130">-Status</span></span>
<span data-ttu-id="114f4-131">Состояние запуска компьютера.</span><span class="sxs-lookup"><span data-stu-id="114f4-131">Status of the machine run.</span></span>

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

### <span data-ttu-id="114f4-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="114f4-132">-TargetComputer</span></span>
<span data-ttu-id="114f4-133">конечный компьютер для запуска компьютера.</span><span class="sxs-lookup"><span data-stu-id="114f4-133">target computer for the machine run.</span></span>
<span data-ttu-id="114f4-134">Может быть либо именем компьютера, не являющимся AZ, либо идентификатором ресурса виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="114f4-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

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

### <span data-ttu-id="114f4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="114f4-135">CommonParameters</span></span>
<span data-ttu-id="114f4-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="114f4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="114f4-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="114f4-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="114f4-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="114f4-138">INPUTS</span></span>

### <span data-ttu-id="114f4-139">System. GUID</span><span class="sxs-lookup"><span data-stu-id="114f4-139">System.Guid</span></span>

### <span data-ttu-id="114f4-140">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="114f4-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="114f4-141">System. Nullable "1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateMachineRunStatus, Microsoft. Azure. командлеты = нейтральный, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="114f4-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="114f4-142">System. String</span><span class="sxs-lookup"><span data-stu-id="114f4-142">System.String</span></span>

## <span data-ttu-id="114f4-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="114f4-143">OUTPUTS</span></span>

### <span data-ttu-id="114f4-144">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="114f4-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="114f4-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="114f4-145">NOTES</span></span>

## <span data-ttu-id="114f4-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="114f4-146">RELATED LINKS</span></span>
