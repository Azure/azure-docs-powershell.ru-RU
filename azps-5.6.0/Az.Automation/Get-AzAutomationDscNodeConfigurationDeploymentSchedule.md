---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: 3bb0f095550394991bb74065e8d1c34c346b0c4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954899"
---
# <span data-ttu-id="24d5a-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="24d5a-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="24d5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24d5a-102">SYNOPSIS</span></span>
<span data-ttu-id="24d5a-103">Получает расписание задания развертывания узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="24d5a-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="24d5a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="24d5a-104">SYNTAX</span></span>

### <span data-ttu-id="24d5a-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="24d5a-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24d5a-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="24d5a-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24d5a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24d5a-107">DESCRIPTION</span></span>
<span data-ttu-id="24d5a-108">Чтобы развернуть конфигурацию узла APS Desired State Configuration (DSC) в Azure Automation, можно получить состояние **APSAutomationDscNodeConfigurationDeployment.**</span><span class="sxs-lookup"><span data-stu-id="24d5a-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="24d5a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="24d5a-109">EXAMPLES</span></span>

### <span data-ttu-id="24d5a-110">Пример 1. Получить все расписания развертывания</span><span class="sxs-lookup"><span data-stu-id="24d5a-110">Example 1: Get all the deployment schedules</span></span>
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

### <span data-ttu-id="24d5a-111">Пример 2. Просмотр расписания развертывания</span><span class="sxs-lookup"><span data-stu-id="24d5a-111">Example 2: Get a deployment schedule</span></span>
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

<span data-ttu-id="24d5a-112">Вышеуказанная команда развертывает конфигурацию узла DSC "Config01.Node1" в заданном двумерном массиве имен узлов.</span><span class="sxs-lookup"><span data-stu-id="24d5a-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="24d5a-113">Развертывание происходит поэтапно.</span><span class="sxs-lookup"><span data-stu-id="24d5a-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="24d5a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24d5a-114">PARAMETERS</span></span>

### <span data-ttu-id="24d5a-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="24d5a-115">-AutomationAccountName</span></span>
<span data-ttu-id="24d5a-116">Указывает имя учетной записи автоматизации, которая содержит конфигурацию DSC, которую составляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24d5a-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="24d5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d5a-117">-DefaultProfile</span></span>
<span data-ttu-id="24d5a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="24d5a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24d5a-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="24d5a-119">-JobScheduleId</span></span>
<span data-ttu-id="24d5a-120">Определяет id расписания задания для существующего запланированного задания развертывания.</span><span class="sxs-lookup"><span data-stu-id="24d5a-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

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

### <span data-ttu-id="24d5a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d5a-121">-ResourceGroupName</span></span>
<span data-ttu-id="24d5a-122">Определяет имя группы ресурсов, в которой этот cmdlet составляет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="24d5a-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="24d5a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d5a-123">CommonParameters</span></span>
<span data-ttu-id="24d5a-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24d5a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d5a-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d5a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d5a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="24d5a-126">INPUTS</span></span>

### <span data-ttu-id="24d5a-127">System.Guid</span><span class="sxs-lookup"><span data-stu-id="24d5a-127">System.Guid</span></span>

### <span data-ttu-id="24d5a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="24d5a-128">System.String</span></span>

## <span data-ttu-id="24d5a-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="24d5a-129">OUTPUTS</span></span>

### <span data-ttu-id="24d5a-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="24d5a-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="24d5a-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="24d5a-131">NOTES</span></span>

## <span data-ttu-id="24d5a-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24d5a-132">RELATED LINKS</span></span>

[<span data-ttu-id="24d5a-133">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="24d5a-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="24d5a-134">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="24d5a-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="24d5a-135">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="24d5a-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="24d5a-136">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="24d5a-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="24d5a-137">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="24d5a-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)
