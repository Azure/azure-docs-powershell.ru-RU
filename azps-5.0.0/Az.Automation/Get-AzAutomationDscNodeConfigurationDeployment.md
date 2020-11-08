---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 449d539b767883bb075bcf333695b3285e047a9c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246123"
---
# <span data-ttu-id="bd35d-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="bd35d-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="bd35d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd35d-102">SYNOPSIS</span></span>
<span data-ttu-id="bd35d-103">Возвращает развертывание конфигурации узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="bd35d-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="bd35d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd35d-104">SYNTAX</span></span>

### <span data-ttu-id="bd35d-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd35d-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd35d-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="bd35d-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd35d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd35d-107">DESCRIPTION</span></span>
<span data-ttu-id="bd35d-108">Командлет **Get-AzAutomationDscNodeConfigurationDeployment** развертывает конфигурацию узла AP Desired State Configuration (DSC) в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="bd35d-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="bd35d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd35d-109">EXAMPLES</span></span>

### <span data-ttu-id="bd35d-110">Пример 1: получение развертывания конфигурации узла</span><span class="sxs-lookup"><span data-stu-id="bd35d-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzAutomationDscNodeConfigurationDeployment `
                         -JobId 35b14eb4-52b7-4a1d-ad62-8e9f84adc657 `
                         -AutomationAccountName "Contoso01"  `
                         -ResourceGroupName "ResourceGroup01" `
            
ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : Running
NodeStatus            : {System.Collections.Generic.Dictionary`2[System.String,System.String], System.Collections.Generic.Dictionary`2[System.String,System.String]}
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000

PS C:\> $deployment | Select -expand nodeStatus

Key        Value
---        -----
WebServer  Pending
WebServer2 Pending
WebServer3 Compliant
```

<span data-ttu-id="bd35d-111">Приведенная выше команда развертывает конфигурацию узла DSC с именем "Config01. NODE1" в данном двухмерном многомерном массиве имен узлов.</span><span class="sxs-lookup"><span data-stu-id="bd35d-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="bd35d-112">Развертывание происходит поэтапным образом.</span><span class="sxs-lookup"><span data-stu-id="bd35d-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="bd35d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd35d-113">PARAMETERS</span></span>

### <span data-ttu-id="bd35d-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bd35d-114">-AutomationAccountName</span></span>
<span data-ttu-id="bd35d-115">Указывает имя учетной записи автоматизации, содержащей конфигурацию DSC, которая компилируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="bd35d-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="bd35d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd35d-116">-DefaultProfile</span></span>
<span data-ttu-id="bd35d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bd35d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd35d-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="bd35d-118">-EndTime</span></span>
<span data-ttu-id="bd35d-119">Фильтр по времени окончания.</span><span class="sxs-lookup"><span data-stu-id="bd35d-119">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd35d-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="bd35d-120">-JobId</span></span>
<span data-ttu-id="bd35d-121">Указывает код задания для существующего задания развертывания.</span><span class="sxs-lookup"><span data-stu-id="bd35d-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="bd35d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd35d-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd35d-123">Указывает имя группы ресурсов, в которой этот командлет компилирует конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="bd35d-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="bd35d-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bd35d-124">-StartTime</span></span>
<span data-ttu-id="bd35d-125">Начало фильтра времени начала.</span><span class="sxs-lookup"><span data-stu-id="bd35d-125">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd35d-126">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="bd35d-126">-Status</span></span>
<span data-ttu-id="bd35d-127">Состояние фильтра заданий.</span><span class="sxs-lookup"><span data-stu-id="bd35d-127">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd35d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd35d-128">CommonParameters</span></span>
<span data-ttu-id="bd35d-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd35d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd35d-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd35d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd35d-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd35d-131">INPUTS</span></span>

### <span data-ttu-id="bd35d-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="bd35d-132">System.Guid</span></span>

### <span data-ttu-id="bd35d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bd35d-133">System.String</span></span>

## <span data-ttu-id="bd35d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd35d-134">OUTPUTS</span></span>

### <span data-ttu-id="bd35d-135">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="bd35d-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="bd35d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd35d-136">NOTES</span></span>

## <span data-ttu-id="bd35d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd35d-137">RELATED LINKS</span></span>

[<span data-ttu-id="bd35d-138">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="bd35d-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="bd35d-139">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd35d-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="bd35d-140">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="bd35d-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="bd35d-141">Остановить-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="bd35d-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="bd35d-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="bd35d-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
