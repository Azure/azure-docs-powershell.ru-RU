---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 61018e7713f2e19da646b69d75c89699da86a0c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561939"
---
# <span data-ttu-id="d69c1-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d69c1-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="d69c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d69c1-102">SYNOPSIS</span></span>
<span data-ttu-id="d69c1-103">Развертывает конфигурацию узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d69c1-103">Deploys a DSC Node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d69c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d69c1-104">SYNTAX</span></span>

### <span data-ttu-id="d69c1-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d69c1-105">ByAll (Default)</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d69c1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d69c1-106">ByInputObject</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d69c1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d69c1-107">DESCRIPTION</span></span>
<span data-ttu-id="d69c1-108">Командлет **Start-AzureRmAutomationDscNodeConfigurationDeployment** развертывает конфигурацию узла Desired State Configuration (DSC) в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d69c1-108">The **Start-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="d69c1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d69c1-109">EXAMPLES</span></span>

### <span data-ttu-id="d69c1-110">Пример 1: развертывание конфигурации узла Azure DSC в автоматизации</span><span class="sxs-lookup"><span data-stu-id="d69c1-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="d69c1-111">Приведенная выше команда развертывает конфигурацию узла DSC с именем "Config01. NODE1" в данном двухмерном многомерном массиве имен узлов.</span><span class="sxs-lookup"><span data-stu-id="d69c1-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="d69c1-112">Развертывание происходит поэтапным образом.</span><span class="sxs-lookup"><span data-stu-id="d69c1-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="d69c1-113">Пример 2: планирование развертывания конфигурации узла Azure DSC в автоматизации</span><span class="sxs-lookup"><span data-stu-id="d69c1-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzureRmAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="d69c1-114">Вышеприведенная команда планирует развертывание конфигурации узла DSC с именем "Config01. NODE1" для данного двумерного массива имен узлов.</span><span class="sxs-lookup"><span data-stu-id="d69c1-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="d69c1-115">Развертывание происходит поэтапно и будет выполнено на основании расписания.</span><span class="sxs-lookup"><span data-stu-id="d69c1-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="d69c1-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d69c1-116">PARAMETERS</span></span>

### <span data-ttu-id="d69c1-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d69c1-117">-AutomationAccountName</span></span>
<span data-ttu-id="d69c1-118">Указывает имя учетной записи автоматизации, содержащей конфигурацию DSC, которая компилируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d69c1-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d69c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d69c1-119">-DefaultProfile</span></span>
<span data-ttu-id="d69c1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d69c1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69c1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d69c1-121">-Force</span></span>
<span data-ttu-id="d69c1-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="d69c1-122">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69c1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d69c1-123">-InputObject</span></span>
<span data-ttu-id="d69c1-124">Объект ввода для трубопроводов</span><span class="sxs-lookup"><span data-stu-id="d69c1-124">Input object for Piping</span></span>

```yaml
Type: NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d69c1-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d69c1-125">-NodeConfigurationName</span></span>
<span data-ttu-id="d69c1-126">Указывает имя конфигурации узла DSC, которое развертывается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d69c1-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

```yaml
Type: String
Parameter Sets: ByAll
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d69c1-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="d69c1-127">-NodeName</span></span>
<span data-ttu-id="d69c1-128">Указывает имена узлов, в которых будет развернута Конфигурация узла.</span><span class="sxs-lookup"><span data-stu-id="d69c1-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

```yaml
Type: String[][]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69c1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d69c1-129">-ResourceGroupName</span></span>
<span data-ttu-id="d69c1-130">Указывает имя группы ресурсов, в которой этот командлет компилирует конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="d69c1-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d69c1-131">-Планирование</span><span class="sxs-lookup"><span data-stu-id="d69c1-131">-Schedule</span></span>
<span data-ttu-id="d69c1-132">Объект расписания автоматизации для планирования задания на развертывание.</span><span class="sxs-lookup"><span data-stu-id="d69c1-132">Automation Schedule object to schedule the deployment job.</span></span>

```yaml
Type: Schedule
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69c1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d69c1-133">-Confirm</span></span>
<span data-ttu-id="d69c1-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d69c1-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69c1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d69c1-135">-WhatIf</span></span>
<span data-ttu-id="d69c1-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d69c1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d69c1-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d69c1-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d69c1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69c1-138">CommonParameters</span></span>
<span data-ttu-id="d69c1-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d69c1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69c1-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d69c1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69c1-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d69c1-141">INPUTS</span></span>

### <span data-ttu-id="d69c1-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="d69c1-142">None</span></span>
<span data-ttu-id="d69c1-143">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d69c1-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d69c1-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d69c1-144">OUTPUTS</span></span>

### <span data-ttu-id="d69c1-145">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d69c1-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="d69c1-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="d69c1-146">NOTES</span></span>

## <span data-ttu-id="d69c1-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d69c1-147">RELATED LINKS</span></span>

[<span data-ttu-id="d69c1-148">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="d69c1-148">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="d69c1-149">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d69c1-149">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="d69c1-150">Остановить-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d69c1-150">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="d69c1-151">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="d69c1-151">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="d69c1-152">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="d69c1-152">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="d69c1-153">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="d69c1-153">New-AzureRmAutomationSchedule</span></span>](./New-AzureRmAutomationSchedule.md)
