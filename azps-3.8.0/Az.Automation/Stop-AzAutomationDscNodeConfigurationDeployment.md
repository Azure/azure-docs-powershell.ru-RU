---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3e5ec84dd3560c07fbf68c6f566b4691c1f6e512
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064938"
---
# <span data-ttu-id="ce09b-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ce09b-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="ce09b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce09b-102">SYNOPSIS</span></span>
<span data-ttu-id="ce09b-103">Останавливает развертывание конфигурации узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ce09b-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="ce09b-104">Оно только останавливает текущее задание развертывания, но не отменяет уже назначенные конфигурации узла.</span><span class="sxs-lookup"><span data-stu-id="ce09b-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="ce09b-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce09b-105">SYNTAX</span></span>

### <span data-ttu-id="ce09b-106">ByJobId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ce09b-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce09b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ce09b-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce09b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce09b-108">DESCRIPTION</span></span>
<span data-ttu-id="ce09b-109">Командлет **Stop-AzAutomationDscNodeConfigurationDeployment** останавливает развертывание конфигурации нужной конфигурации узла (DSC) в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ce09b-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="ce09b-110">Она прекращает назначение конфигурации узла группам узлов, если они остаются назначенными, но не отменяют назначение уже назначенным узлам.</span><span class="sxs-lookup"><span data-stu-id="ce09b-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="ce09b-111">Чтобы отменить регистрацию запланированного задания, используйте параметр [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) с параметром JobScheduleId для отмены назначения существующего запланированного задания.</span><span class="sxs-lookup"><span data-stu-id="ce09b-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="ce09b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce09b-112">EXAMPLES</span></span>

### <span data-ttu-id="ce09b-113">Пример 1: развертывание конфигурации узла Azure DSC в автоматизации</span><span class="sxs-lookup"><span data-stu-id="ce09b-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="ce09b-114">Указанная выше команда останавливает задание развертывания конфигурации узла DSC с переданным jobId.</span><span class="sxs-lookup"><span data-stu-id="ce09b-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="ce09b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce09b-115">PARAMETERS</span></span>

### <span data-ttu-id="ce09b-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ce09b-116">-AutomationAccountName</span></span>
<span data-ttu-id="ce09b-117">Указывает имя учетной записи автоматизации, содержащей конфигурацию DSC, которая компилируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ce09b-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="ce09b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce09b-118">-DefaultProfile</span></span>
<span data-ttu-id="ce09b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ce09b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce09b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ce09b-120">-Force</span></span>
<span data-ttu-id="ce09b-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="ce09b-121">ps_force</span></span>

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

### <span data-ttu-id="ce09b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce09b-122">-InputObject</span></span>
<span data-ttu-id="ce09b-123">Объект ввода для трубопроводов</span><span class="sxs-lookup"><span data-stu-id="ce09b-123">Input object for Piping</span></span>

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

### <span data-ttu-id="ce09b-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="ce09b-124">-JobId</span></span>
<span data-ttu-id="ce09b-125">Указывает код задания для существующего задания развертывания.</span><span class="sxs-lookup"><span data-stu-id="ce09b-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="ce09b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce09b-126">-PassThru</span></span>
<span data-ttu-id="ce09b-127">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="ce09b-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ce09b-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="ce09b-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ce09b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce09b-129">-ResourceGroupName</span></span>
<span data-ttu-id="ce09b-130">Указывает имя группы ресурсов, в которой этот командлет компилирует конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ce09b-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="ce09b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce09b-131">-Confirm</span></span>
<span data-ttu-id="ce09b-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ce09b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce09b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce09b-133">-WhatIf</span></span>
<span data-ttu-id="ce09b-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ce09b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce09b-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ce09b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce09b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce09b-136">CommonParameters</span></span>
<span data-ttu-id="ce09b-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce09b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce09b-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce09b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce09b-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce09b-139">INPUTS</span></span>

### <span data-ttu-id="ce09b-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ce09b-140">System.Guid</span></span>

### <span data-ttu-id="ce09b-141">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ce09b-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="ce09b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ce09b-142">System.String</span></span>

## <span data-ttu-id="ce09b-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce09b-143">OUTPUTS</span></span>

### <span data-ttu-id="ce09b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce09b-144">System.Boolean</span></span>

## <span data-ttu-id="ce09b-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce09b-145">NOTES</span></span>

## <span data-ttu-id="ce09b-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce09b-146">RELATED LINKS</span></span>

[<span data-ttu-id="ce09b-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="ce09b-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="ce09b-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce09b-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="ce09b-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ce09b-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="ce09b-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ce09b-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="ce09b-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="ce09b-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
