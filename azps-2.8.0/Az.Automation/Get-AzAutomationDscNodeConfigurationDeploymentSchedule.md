---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: 2ae7f5099db2f9aee0c6f6e86e3dba690aa61454
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727856"
---
# <span data-ttu-id="77d6f-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="77d6f-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="77d6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="77d6f-103">Возвращает расписание заданий развертывания конфигурации узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="77d6f-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="77d6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77d6f-104">SYNTAX</span></span>

### <span data-ttu-id="77d6f-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77d6f-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77d6f-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="77d6f-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77d6f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77d6f-107">DESCRIPTION</span></span>
<span data-ttu-id="77d6f-108">Командлет **Get-AzAutomationDscNodeConfigurationDeployment** развертывает конфигурацию узла AP Desired State Configuration (DSC) в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="77d6f-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="77d6f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77d6f-109">EXAMPLES</span></span>

### <span data-ttu-id="77d6f-110">Пример 1: получение всех расписаний развертывания</span><span class="sxs-lookup"><span data-stu-id="77d6f-110">Example 1: Get all the deployment schedules</span></span>
```
PS C:\> Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01"

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : e347dfc4-62fe-4ed6-adfb-55518c57b558
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
```

### <span data-ttu-id="77d6f-111">Пример 2: получение расписания развертывания</span><span class="sxs-lookup"><span data-stu-id="77d6f-111">Example 2: Get a deployment schedule</span></span>
```
PS C:\> $js= Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
                 -AutomationAccountName "Contoso01" `
                 -ResourceGroupName "ResourceGroup01" `
                 -JobScheduleId 2b1d7738-093d-4ff7-b87b-e4b2321319e5

PS C:\> $js

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSche
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

PS C:\> $js.JobSchedule

ResourceGroupName     : ResourceGroup01
RunOn                 :
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
ScheduleName          : TestScheduleName
Parameters            : {AutomationAccountName, NodeConfigurationName, ResourceGroupName, ListOfNodeNames}
HybridWorker          :
```

<span data-ttu-id="77d6f-112">Приведенная выше команда развертывает конфигурацию узла DSC с именем "Config01. NODE1" в данном двухмерном многомерном массиве имен узлов.</span><span class="sxs-lookup"><span data-stu-id="77d6f-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="77d6f-113">Развертывание происходит поэтапным образом.</span><span class="sxs-lookup"><span data-stu-id="77d6f-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="77d6f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77d6f-114">PARAMETERS</span></span>

### <span data-ttu-id="77d6f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="77d6f-115">-AutomationAccountName</span></span>
<span data-ttu-id="77d6f-116">Указывает имя учетной записи автоматизации, содержащей конфигурацию DSC, которая компилируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="77d6f-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="77d6f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77d6f-117">-DefaultProfile</span></span>
<span data-ttu-id="77d6f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="77d6f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="77d6f-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="77d6f-119">-JobScheduleId</span></span>
<span data-ttu-id="77d6f-120">Указывает идентификатор расписания задания для существующего запланированного задания развертывания.</span><span class="sxs-lookup"><span data-stu-id="77d6f-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77d6f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77d6f-121">-ResourceGroupName</span></span>
<span data-ttu-id="77d6f-122">Указывает имя группы ресурсов, в которой этот командлет компилирует конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="77d6f-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="77d6f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d6f-123">CommonParameters</span></span>
<span data-ttu-id="77d6f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77d6f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d6f-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77d6f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d6f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77d6f-126">INPUTS</span></span>

### <span data-ttu-id="77d6f-127">System. GUID</span><span class="sxs-lookup"><span data-stu-id="77d6f-127">System.Guid</span></span>

### <span data-ttu-id="77d6f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="77d6f-128">System.String</span></span>

## <span data-ttu-id="77d6f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77d6f-129">OUTPUTS</span></span>

### <span data-ttu-id="77d6f-130">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="77d6f-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="77d6f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="77d6f-131">NOTES</span></span>

## <span data-ttu-id="77d6f-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77d6f-132">RELATED LINKS</span></span>

[<span data-ttu-id="77d6f-133">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="77d6f-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="77d6f-134">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="77d6f-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="77d6f-135">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="77d6f-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="77d6f-136">Остановить-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="77d6f-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="77d6f-137">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="77d6f-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)
