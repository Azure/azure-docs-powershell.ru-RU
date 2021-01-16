---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: bc98d8ed8773e49eab594a4d715bef3f93862e83
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418716"
---
# <span data-ttu-id="f69b7-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="f69b7-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="f69b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f69b7-102">SYNOPSIS</span></span>
<span data-ttu-id="f69b7-103">Получает расписание задания развертывания узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="f69b7-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="f69b7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f69b7-104">SYNTAX</span></span>

### <span data-ttu-id="f69b7-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f69b7-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f69b7-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="f69b7-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f69b7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f69b7-107">DESCRIPTION</span></span>
<span data-ttu-id="f69b7-108">Для развертывания конфигурации узла APS в автоматизации Azure развертывается cmdlet **Get-AzAutomationDscNodeConfigurationDeployment.**</span><span class="sxs-lookup"><span data-stu-id="f69b7-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="f69b7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f69b7-109">EXAMPLES</span></span>

### <span data-ttu-id="f69b7-110">Пример 1. Получить все расписания развертывания</span><span class="sxs-lookup"><span data-stu-id="f69b7-110">Example 1: Get all the deployment schedules</span></span>
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

### <span data-ttu-id="f69b7-111">Пример 2. Получите расписание развертывания</span><span class="sxs-lookup"><span data-stu-id="f69b7-111">Example 2: Get a deployment schedule</span></span>
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

<span data-ttu-id="f69b7-112">Вышеуказанная команда развертывает конфигурацию узла DSC "Config01.Node1" в заданном двумерном массиве имен узлов.</span><span class="sxs-lookup"><span data-stu-id="f69b7-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="f69b7-113">Развертывание происходит поэтапно.</span><span class="sxs-lookup"><span data-stu-id="f69b7-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="f69b7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f69b7-114">PARAMETERS</span></span>

### <span data-ttu-id="f69b7-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f69b7-115">-AutomationAccountName</span></span>
<span data-ttu-id="f69b7-116">Указывает имя учетной записи автоматизации, которая содержит конфигурацию DSC, которую составляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f69b7-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="f69b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f69b7-117">-DefaultProfile</span></span>
<span data-ttu-id="f69b7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f69b7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f69b7-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="f69b7-119">-JobScheduleId</span></span>
<span data-ttu-id="f69b7-120">Определяет id расписания задания для существующего запланированного задания развертывания.</span><span class="sxs-lookup"><span data-stu-id="f69b7-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

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

### <span data-ttu-id="f69b7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f69b7-121">-ResourceGroupName</span></span>
<span data-ttu-id="f69b7-122">Определяет имя группы ресурсов, в которой этот cmdlet составляет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f69b7-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="f69b7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f69b7-123">CommonParameters</span></span>
<span data-ttu-id="f69b7-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f69b7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f69b7-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f69b7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f69b7-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f69b7-126">INPUTS</span></span>

### <span data-ttu-id="f69b7-127">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f69b7-127">System.Guid</span></span>

### <span data-ttu-id="f69b7-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f69b7-128">System.String</span></span>

## <span data-ttu-id="f69b7-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f69b7-129">OUTPUTS</span></span>

### <span data-ttu-id="f69b7-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="f69b7-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="f69b7-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f69b7-131">NOTES</span></span>

## <span data-ttu-id="f69b7-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f69b7-132">RELATED LINKS</span></span>

[<span data-ttu-id="f69b7-133">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="f69b7-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="f69b7-134">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="f69b7-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="f69b7-135">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f69b7-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="f69b7-136">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f69b7-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="f69b7-137">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="f69b7-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)
