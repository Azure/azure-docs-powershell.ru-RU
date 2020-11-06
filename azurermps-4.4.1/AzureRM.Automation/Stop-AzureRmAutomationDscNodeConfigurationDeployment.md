---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3ddaf0d4ae609305bf9740fbbe38a5fddd414e18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568340"
---
# <span data-ttu-id="744c6-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="744c6-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="744c6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="744c6-102">SYNOPSIS</span></span>
<span data-ttu-id="744c6-103">Останавливает развертывание конфигурации узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="744c6-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="744c6-104">Оно только останавливает текущее задание развертывания, но не отменяет уже назначенные конфигурации узла.</span><span class="sxs-lookup"><span data-stu-id="744c6-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="744c6-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="744c6-105">SYNTAX</span></span>

### <span data-ttu-id="744c6-106">ByJobId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="744c6-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="744c6-107">ByByInputObject</span><span class="sxs-lookup"><span data-stu-id="744c6-107">ByByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> -AutomationAccountName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="744c6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="744c6-108">DESCRIPTION</span></span>
<span data-ttu-id="744c6-109">Командлет **Stop-AzureRmAutomationDscNodeConfigurationDeployment** останавливает развертывание конфигурации нужной конфигурации узла (DSC) в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="744c6-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="744c6-110">Она прекращает назначение конфигурации узла группам узлов, если они остаются назначенными, но не отменяют назначение уже назначенным узлам.</span><span class="sxs-lookup"><span data-stu-id="744c6-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="744c6-111">Чтобы отменить регистрацию запланированного задания, используйте параметр [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) с параметром JobScheduleId для отмены назначения существующего запланированного задания.</span><span class="sxs-lookup"><span data-stu-id="744c6-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="744c6-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="744c6-112">EXAMPLES</span></span>

### <span data-ttu-id="744c6-113">Пример 1: развертывание конфигурации узла Azure DSC в автоматизации</span><span class="sxs-lookup"><span data-stu-id="744c6-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="744c6-114">Указанная выше команда останавливает задание развертывания конфигурации узла DSC с переданным jobId.</span><span class="sxs-lookup"><span data-stu-id="744c6-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="744c6-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="744c6-115">PARAMETERS</span></span>

### <span data-ttu-id="744c6-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="744c6-116">-AutomationAccountName</span></span>
<span data-ttu-id="744c6-117">Указывает имя учетной записи автоматизации, содержащей конфигурацию DSC, которая компилируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="744c6-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="744c6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="744c6-118">-ResourceGroupName</span></span>
<span data-ttu-id="744c6-119">Указывает имя группы ресурсов, в которой этот командлет компилирует конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="744c6-119">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="744c6-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="744c6-120">-JobId</span></span>
<span data-ttu-id="744c6-121">Указывает код задания для существующего задания развертывания.</span><span class="sxs-lookup"><span data-stu-id="744c6-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="744c6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="744c6-122">-PassThru</span></span>
<span data-ttu-id="744c6-123">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="744c6-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="744c6-124">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="744c6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="744c6-125">-Force</span><span class="sxs-lookup"><span data-stu-id="744c6-125">-Force</span></span>
<span data-ttu-id="744c6-126">ps_force</span><span class="sxs-lookup"><span data-stu-id="744c6-126">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="744c6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="744c6-127">-Confirm</span></span>
<span data-ttu-id="744c6-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="744c6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="744c6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="744c6-129">-WhatIf</span></span>
<span data-ttu-id="744c6-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="744c6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="744c6-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="744c6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="744c6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="744c6-132">-DefaultProfile</span></span>
<span data-ttu-id="744c6-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="744c6-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="744c6-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="744c6-134">-InputObject</span></span>
<span data-ttu-id="744c6-135">Объект ввода для трубопроводов.</span><span class="sxs-lookup"><span data-stu-id="744c6-135">Input object for Piping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="744c6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="744c6-136">CommonParameters</span></span>
<span data-ttu-id="744c6-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="744c6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="744c6-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="744c6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="744c6-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="744c6-139">INPUTS</span></span>

## <span data-ttu-id="744c6-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="744c6-140">OUTPUTS</span></span>

## <span data-ttu-id="744c6-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="744c6-141">NOTES</span></span>

## <span data-ttu-id="744c6-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="744c6-142">RELATED LINKS</span></span>

[<span data-ttu-id="744c6-143">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="744c6-143">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="744c6-144">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="744c6-144">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="744c6-145">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="744c6-145">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="744c6-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="744c6-146">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="744c6-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="744c6-147">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
