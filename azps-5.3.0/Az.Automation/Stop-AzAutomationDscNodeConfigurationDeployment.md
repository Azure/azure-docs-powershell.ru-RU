---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3e5ec84dd3560c07fbf68c6f566b4691c1f6e512
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509825"
---
# <span data-ttu-id="9d5a8-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9d5a8-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="9d5a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="9d5a8-103">Остановка развертывания конфигурации узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="9d5a8-104">Оно только останавливает текущее задание развертывания, но не отогнает уже назначенную конфигурацию узла.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="9d5a8-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9d5a8-105">SYNTAX</span></span>

### <span data-ttu-id="9d5a8-106">ByJobId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d5a8-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d5a8-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9d5a8-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d5a8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d5a8-108">DESCRIPTION</span></span>
<span data-ttu-id="9d5a8-109">Для выполнения настройки узла DSC в Azure выполнение конфигурации узла **Stop-AzAutomationDscNodeConfigurationDeployment** прекращается.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="9d5a8-110">Она останавливает назначение конфигурации узла группам узлов, если они еще не назначены, но не отписает уже назначенные узлы.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="9d5a8-111">Чтобы отоименовать запланированное задание, воспользуйтесь книгой [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) с jobScheduleId, чтобы отоменить существующее запланированное задание.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="9d5a8-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9d5a8-112">EXAMPLES</span></span>

### <span data-ttu-id="9d5a8-113">Пример 1. Развертывание конфигурации узла службы DSC Azure в автоматизации</span><span class="sxs-lookup"><span data-stu-id="9d5a8-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="9d5a8-114">Вышеуказанная команда останавливает задание развертывания конфигурации узла DSC с переданным идом задания.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="9d5a8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d5a8-115">PARAMETERS</span></span>

### <span data-ttu-id="9d5a8-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9d5a8-116">-AutomationAccountName</span></span>
<span data-ttu-id="9d5a8-117">Указывает имя учетной записи автоматизации, которая содержит конфигурацию DSC, которую составляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="9d5a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d5a8-118">-DefaultProfile</span></span>
<span data-ttu-id="9d5a8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9d5a8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d5a8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="9d5a8-120">-Force</span></span>
<span data-ttu-id="9d5a8-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="9d5a8-121">ps_force</span></span>

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

### <span data-ttu-id="9d5a8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d5a8-122">-InputObject</span></span>
<span data-ttu-id="9d5a8-123">Объект ввода для piping</span><span class="sxs-lookup"><span data-stu-id="9d5a8-123">Input object for Piping</span></span>

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

### <span data-ttu-id="9d5a8-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="9d5a8-124">-JobId</span></span>
<span data-ttu-id="9d5a8-125">Указывает ид задания существующего задания развертывания.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="9d5a8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d5a8-126">-PassThru</span></span>
<span data-ttu-id="9d5a8-127">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9d5a8-128">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9d5a8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d5a8-129">-ResourceGroupName</span></span>
<span data-ttu-id="9d5a8-130">Определяет имя группы ресурсов, в которой этот cmdlet составляет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="9d5a8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d5a8-131">-Confirm</span></span>
<span data-ttu-id="9d5a8-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d5a8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d5a8-133">-WhatIf</span></span>
<span data-ttu-id="9d5a8-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d5a8-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d5a8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d5a8-136">CommonParameters</span></span>
<span data-ttu-id="9d5a8-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d5a8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d5a8-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d5a8-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d5a8-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d5a8-139">INPUTS</span></span>

### <span data-ttu-id="9d5a8-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9d5a8-140">System.Guid</span></span>

### <span data-ttu-id="9d5a8-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9d5a8-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="9d5a8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9d5a8-142">System.String</span></span>

## <span data-ttu-id="9d5a8-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d5a8-143">OUTPUTS</span></span>

### <span data-ttu-id="9d5a8-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9d5a8-144">System.Boolean</span></span>

## <span data-ttu-id="9d5a8-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9d5a8-145">NOTES</span></span>

## <span data-ttu-id="9d5a8-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d5a8-146">RELATED LINKS</span></span>

[<span data-ttu-id="9d5a8-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="9d5a8-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="9d5a8-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d5a8-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="9d5a8-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9d5a8-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="9d5a8-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="9d5a8-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="9d5a8-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="9d5a8-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
