---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 41605bbdd37ae29f420581f9ad916a1cc87150be
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077912"
---
# <span data-ttu-id="43b99-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="43b99-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="43b99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43b99-102">SYNOPSIS</span></span>
<span data-ttu-id="43b99-103">Развертывает конфигурацию узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="43b99-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="43b99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43b99-104">SYNTAX</span></span>

### <span data-ttu-id="43b99-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43b99-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43b99-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="43b99-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43b99-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43b99-107">DESCRIPTION</span></span>
<span data-ttu-id="43b99-108">Командлет **Start-AzAutomationDscNodeConfigurationDeployment** развертывает конфигурацию узла Desired State Configuration (DSC) в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="43b99-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="43b99-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43b99-109">EXAMPLES</span></span>

### <span data-ttu-id="43b99-110">Пример 1: развертывание конфигурации узла Azure DSC в автоматизации</span><span class="sxs-lookup"><span data-stu-id="43b99-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
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

<span data-ttu-id="43b99-111">Приведенная выше команда развертывает конфигурацию узла DSC с именем "Config01. NODE1" в данном двухмерном многомерном массиве имен узлов.</span><span class="sxs-lookup"><span data-stu-id="43b99-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="43b99-112">Развертывание происходит поэтапным образом.</span><span class="sxs-lookup"><span data-stu-id="43b99-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="43b99-113">Пример 2: планирование развертывания конфигурации узла Azure DSC в автоматизации</span><span class="sxs-lookup"><span data-stu-id="43b99-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
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

<span data-ttu-id="43b99-114">Вышеприведенная команда планирует развертывание конфигурации узла DSC с именем "Config01. NODE1" для данного двумерного массива имен узлов.</span><span class="sxs-lookup"><span data-stu-id="43b99-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="43b99-115">Развертывание происходит поэтапно и будет выполнено на основании расписания.</span><span class="sxs-lookup"><span data-stu-id="43b99-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="43b99-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43b99-116">PARAMETERS</span></span>

### <span data-ttu-id="43b99-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="43b99-117">-AutomationAccountName</span></span>
<span data-ttu-id="43b99-118">Указывает имя учетной записи автоматизации, содержащей конфигурацию DSC, которая компилируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="43b99-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="43b99-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b99-119">-DefaultProfile</span></span>
<span data-ttu-id="43b99-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="43b99-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43b99-121">-Force</span><span class="sxs-lookup"><span data-stu-id="43b99-121">-Force</span></span>
<span data-ttu-id="43b99-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="43b99-122">ps_force</span></span>

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

### <span data-ttu-id="43b99-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43b99-123">-InputObject</span></span>
<span data-ttu-id="43b99-124">Объект ввода для трубопроводов</span><span class="sxs-lookup"><span data-stu-id="43b99-124">Input object for Piping</span></span>

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

### <span data-ttu-id="43b99-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="43b99-125">-NodeConfigurationName</span></span>
<span data-ttu-id="43b99-126">Указывает имя конфигурации узла DSC, которое развертывается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="43b99-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

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

### <span data-ttu-id="43b99-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="43b99-127">-NodeName</span></span>
<span data-ttu-id="43b99-128">Указывает имена узлов, в которых будет развернута Конфигурация узла.</span><span class="sxs-lookup"><span data-stu-id="43b99-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

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

### <span data-ttu-id="43b99-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43b99-129">-ResourceGroupName</span></span>
<span data-ttu-id="43b99-130">Указывает имя группы ресурсов, в которой этот командлет компилирует конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="43b99-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="43b99-131">-Планирование</span><span class="sxs-lookup"><span data-stu-id="43b99-131">-Schedule</span></span>
<span data-ttu-id="43b99-132">Объект расписания автоматизации для планирования задания на развертывание.</span><span class="sxs-lookup"><span data-stu-id="43b99-132">Automation Schedule object to schedule the deployment job.</span></span>

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

### <span data-ttu-id="43b99-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43b99-133">-Confirm</span></span>
<span data-ttu-id="43b99-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="43b99-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43b99-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43b99-135">-WhatIf</span></span>
<span data-ttu-id="43b99-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="43b99-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43b99-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="43b99-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43b99-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b99-138">CommonParameters</span></span>
<span data-ttu-id="43b99-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43b99-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b99-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43b99-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b99-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43b99-141">INPUTS</span></span>

### <span data-ttu-id="43b99-142">System. String</span><span class="sxs-lookup"><span data-stu-id="43b99-142">System.String</span></span>

### <span data-ttu-id="43b99-143">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="43b99-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="43b99-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43b99-144">OUTPUTS</span></span>

### <span data-ttu-id="43b99-145">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="43b99-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="43b99-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="43b99-146">NOTES</span></span>

## <span data-ttu-id="43b99-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43b99-147">RELATED LINKS</span></span>

[<span data-ttu-id="43b99-148">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="43b99-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="43b99-149">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="43b99-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="43b99-150">Остановить-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="43b99-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="43b99-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="43b99-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="43b99-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="43b99-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="43b99-153">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="43b99-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
