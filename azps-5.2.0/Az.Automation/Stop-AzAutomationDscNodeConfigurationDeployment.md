---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3e5ec84dd3560c07fbf68c6f566b4691c1f6e512
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400668"
---
# <span data-ttu-id="5ccb1-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5ccb1-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="5ccb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ccb1-102">SYNOPSIS</span></span>
<span data-ttu-id="5ccb1-103">Остановка развертывания конфигурации узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="5ccb1-104">Оно только останавливает текущее задание развертывания, но не отогнает уже назначенную конфигурацию узла.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="5ccb1-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ccb1-105">SYNTAX</span></span>

### <span data-ttu-id="5ccb1-106">ByJobId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ccb1-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ccb1-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5ccb1-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ccb1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ccb1-108">DESCRIPTION</span></span>
<span data-ttu-id="5ccb1-109">Для выполнения настройки узла DSC в Azure выполнение конфигурации узла **Stop-AzAutomationDscNodeConfigurationDeployment** прекращается.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="5ccb1-110">Она останавливает назначение конфигурации узла группам узлов, если они еще не назначены, но не отписает уже назначенные узлы.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="5ccb1-111">Чтобы отоименовать запланированное задание, воспользуйтесь книгой [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) с jobScheduleId, чтобы отоменить существующее запланированное задание.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="5ccb1-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ccb1-112">EXAMPLES</span></span>

### <span data-ttu-id="5ccb1-113">Пример 1. Развертывание конфигурации узла службы DSC Azure в автоматизации</span><span class="sxs-lookup"><span data-stu-id="5ccb1-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="5ccb1-114">Вышеуказанная команда останавливает задание развертывания конфигурации узла DSC с переданным идом.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="5ccb1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ccb1-115">PARAMETERS</span></span>

### <span data-ttu-id="5ccb1-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5ccb1-116">-AutomationAccountName</span></span>
<span data-ttu-id="5ccb1-117">Указывает имя учетной записи автоматизации, которая содержит конфигурацию DSC, которую составляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="5ccb1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ccb1-118">-DefaultProfile</span></span>
<span data-ttu-id="5ccb1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ccb1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ccb1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5ccb1-120">-Force</span></span>
<span data-ttu-id="5ccb1-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="5ccb1-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ccb1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ccb1-122">-InputObject</span></span>
<span data-ttu-id="5ccb1-123">Входной объект для Piping</span><span class="sxs-lookup"><span data-stu-id="5ccb1-123">Input object for Piping</span></span>

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

### <span data-ttu-id="5ccb1-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="5ccb1-124">-JobId</span></span>
<span data-ttu-id="5ccb1-125">Указывает ид задания существующего задания развертывания.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-125">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ccb1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ccb1-126">-PassThru</span></span>
<span data-ttu-id="5ccb1-127">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5ccb1-128">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ccb1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ccb1-129">-ResourceGroupName</span></span>
<span data-ttu-id="5ccb1-130">Определяет имя группы ресурсов, в которой этот cmdlet составляет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="5ccb1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ccb1-131">-Confirm</span></span>
<span data-ttu-id="5ccb1-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ccb1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ccb1-133">-WhatIf</span></span>
<span data-ttu-id="5ccb1-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ccb1-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ccb1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ccb1-136">CommonParameters</span></span>
<span data-ttu-id="5ccb1-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ccb1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ccb1-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ccb1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ccb1-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ccb1-139">INPUTS</span></span>

### <span data-ttu-id="5ccb1-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5ccb1-140">System.Guid</span></span>

### <span data-ttu-id="5ccb1-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5ccb1-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="5ccb1-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5ccb1-142">System.String</span></span>

## <span data-ttu-id="5ccb1-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ccb1-143">OUTPUTS</span></span>

### <span data-ttu-id="5ccb1-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ccb1-144">System.Boolean</span></span>

## <span data-ttu-id="5ccb1-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ccb1-145">NOTES</span></span>

## <span data-ttu-id="5ccb1-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ccb1-146">RELATED LINKS</span></span>

[<span data-ttu-id="5ccb1-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5ccb1-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="5ccb1-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ccb1-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="5ccb1-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5ccb1-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5ccb1-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5ccb1-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5ccb1-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="5ccb1-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
