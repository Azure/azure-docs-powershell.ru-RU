---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 41605bbdd37ae29f420581f9ad916a1cc87150be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235060"
---
# <span data-ttu-id="df895-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="df895-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="df895-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df895-102">SYNOPSIS</span></span>
<span data-ttu-id="df895-103">Развертывает конфигурацию узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="df895-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="df895-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="df895-104">SYNTAX</span></span>

### <span data-ttu-id="df895-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df895-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df895-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="df895-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df895-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df895-107">DESCRIPTION</span></span>
<span data-ttu-id="df895-108">Для выполнения настройки узла **Start-AzAutomationDscNodeConfigurationDeployment** в Azure Automation развертывается конфигурация узла DSC.</span><span class="sxs-lookup"><span data-stu-id="df895-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="df895-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="df895-109">EXAMPLES</span></span>

### <span data-ttu-id="df895-110">Пример 1. Развертывание конфигурации узла службы DSC Azure в автоматизации</span><span class="sxs-lookup"><span data-stu-id="df895-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Yes

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : New
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="df895-111">Вышеуказанная команда развертывает конфигурацию узла DSC "Config01.Node1" в заданном двумерном массиве имен узлов.</span><span class="sxs-lookup"><span data-stu-id="df895-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="df895-112">Развертывание происходит поэтапно.</span><span class="sxs-lookup"><span data-stu-id="df895-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="df895-113">Пример 2. Запланировать развертывание конфигурации узла Azure DSC в автоматизации</span><span class="sxs-lookup"><span data-stu-id="df895-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `
            -Schedule $sched

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 00000000-0000-0000-0000-000000000000
Job                   :
JobStatus             :
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
```

<span data-ttu-id="df895-114">С этой командой можно запланировать развертывание конфигурации узла DSC с именем "Config01.Node1" в заданном двумерном массиве имен узлов.</span><span class="sxs-lookup"><span data-stu-id="df895-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="df895-115">Развертывание выполняется поэтапно и будет выполняться согласно расписанию.</span><span class="sxs-lookup"><span data-stu-id="df895-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="df895-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df895-116">PARAMETERS</span></span>

### <span data-ttu-id="df895-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="df895-117">-AutomationAccountName</span></span>
<span data-ttu-id="df895-118">Указывает имя учетной записи автоматизации, которая содержит конфигурацию DSC, которую составляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df895-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="df895-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df895-119">-DefaultProfile</span></span>
<span data-ttu-id="df895-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="df895-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df895-121">-Force</span><span class="sxs-lookup"><span data-stu-id="df895-121">-Force</span></span>
<span data-ttu-id="df895-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="df895-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df895-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df895-123">-InputObject</span></span>
<span data-ttu-id="df895-124">Входной объект для Piping</span><span class="sxs-lookup"><span data-stu-id="df895-124">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df895-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="df895-125">-NodeConfigurationName</span></span>
<span data-ttu-id="df895-126">Указывает имя конфигурации узла DSC, которую развертывает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df895-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df895-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="df895-127">-NodeName</span></span>
<span data-ttu-id="df895-128">Указывает имена узлов, для которых будет развернута конфигурация узла.</span><span class="sxs-lookup"><span data-stu-id="df895-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

```yaml
Type: System.String[][]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df895-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df895-129">-ResourceGroupName</span></span>
<span data-ttu-id="df895-130">Определяет имя группы ресурсов, в которой этот cmdlet составляет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="df895-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="df895-131">-Расписание</span><span class="sxs-lookup"><span data-stu-id="df895-131">-Schedule</span></span>
<span data-ttu-id="df895-132">Объект "Расписание автоматизации", чтобы запланировать задание развертывания.</span><span class="sxs-lookup"><span data-stu-id="df895-132">Automation Schedule object to schedule the deployment job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df895-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df895-133">-Confirm</span></span>
<span data-ttu-id="df895-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="df895-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df895-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df895-135">-WhatIf</span></span>
<span data-ttu-id="df895-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df895-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df895-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="df895-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df895-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df895-138">CommonParameters</span></span>
<span data-ttu-id="df895-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df895-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df895-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df895-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df895-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df895-141">INPUTS</span></span>

### <span data-ttu-id="df895-142">System.String</span><span class="sxs-lookup"><span data-stu-id="df895-142">System.String</span></span>

### <span data-ttu-id="df895-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="df895-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="df895-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="df895-144">OUTPUTS</span></span>

### <span data-ttu-id="df895-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="df895-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="df895-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="df895-146">NOTES</span></span>

## <span data-ttu-id="df895-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df895-147">RELATED LINKS</span></span>

[<span data-ttu-id="df895-148">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="df895-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="df895-149">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="df895-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="df895-150">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="df895-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="df895-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="df895-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="df895-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="df895-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="df895-153">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="df895-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
