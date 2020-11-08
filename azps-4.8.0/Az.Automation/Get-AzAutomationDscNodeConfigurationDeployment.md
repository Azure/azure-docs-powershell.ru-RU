---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 449d539b767883bb075bcf333695b3285e047a9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077965"
---
# <span data-ttu-id="dd95e-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="dd95e-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="dd95e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd95e-102">SYNOPSIS</span></span>
<span data-ttu-id="dd95e-103">Возвращает развертывание конфигурации узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="dd95e-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="dd95e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd95e-104">SYNTAX</span></span>

### <span data-ttu-id="dd95e-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd95e-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd95e-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="dd95e-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd95e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd95e-107">DESCRIPTION</span></span>
<span data-ttu-id="dd95e-108">Командлет **Get-AzAutomationDscNodeConfigurationDeployment** развертывает конфигурацию узла AP Desired State Configuration (DSC) в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="dd95e-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="dd95e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd95e-109">EXAMPLES</span></span>

### <span data-ttu-id="dd95e-110">Пример 1: получение развертывания конфигурации узла</span><span class="sxs-lookup"><span data-stu-id="dd95e-110">Example 1: Get a node configuration deployment</span></span>
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

<span data-ttu-id="dd95e-111">Приведенная выше команда развертывает конфигурацию узла DSC с именем "Config01. NODE1" в данном двухмерном многомерном массиве имен узлов.</span><span class="sxs-lookup"><span data-stu-id="dd95e-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="dd95e-112">Развертывание происходит поэтапным образом.</span><span class="sxs-lookup"><span data-stu-id="dd95e-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="dd95e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd95e-113">PARAMETERS</span></span>

### <span data-ttu-id="dd95e-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dd95e-114">-AutomationAccountName</span></span>
<span data-ttu-id="dd95e-115">Указывает имя учетной записи автоматизации, содержащей конфигурацию DSC, которая компилируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="dd95e-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="dd95e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd95e-116">-DefaultProfile</span></span>
<span data-ttu-id="dd95e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="dd95e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd95e-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="dd95e-118">-EndTime</span></span>
<span data-ttu-id="dd95e-119">Фильтр по времени окончания.</span><span class="sxs-lookup"><span data-stu-id="dd95e-119">End time filter.</span></span>

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

### <span data-ttu-id="dd95e-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="dd95e-120">-JobId</span></span>
<span data-ttu-id="dd95e-121">Указывает код задания для существующего задания развертывания.</span><span class="sxs-lookup"><span data-stu-id="dd95e-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="dd95e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd95e-122">-ResourceGroupName</span></span>
<span data-ttu-id="dd95e-123">Указывает имя группы ресурсов, в которой этот командлет компилирует конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="dd95e-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="dd95e-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="dd95e-124">-StartTime</span></span>
<span data-ttu-id="dd95e-125">Начало фильтра времени начала.</span><span class="sxs-lookup"><span data-stu-id="dd95e-125">Start time filter.</span></span>

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

### <span data-ttu-id="dd95e-126">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="dd95e-126">-Status</span></span>
<span data-ttu-id="dd95e-127">Состояние фильтра заданий.</span><span class="sxs-lookup"><span data-stu-id="dd95e-127">Status of the Job filter.</span></span>

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

### <span data-ttu-id="dd95e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd95e-128">CommonParameters</span></span>
<span data-ttu-id="dd95e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd95e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd95e-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd95e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd95e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd95e-131">INPUTS</span></span>

### <span data-ttu-id="dd95e-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="dd95e-132">System.Guid</span></span>

### <span data-ttu-id="dd95e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dd95e-133">System.String</span></span>

## <span data-ttu-id="dd95e-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd95e-134">OUTPUTS</span></span>

### <span data-ttu-id="dd95e-135">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="dd95e-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="dd95e-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd95e-136">NOTES</span></span>

## <span data-ttu-id="dd95e-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd95e-137">RELATED LINKS</span></span>

[<span data-ttu-id="dd95e-138">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="dd95e-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="dd95e-139">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="dd95e-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="dd95e-140">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="dd95e-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="dd95e-141">Остановить-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="dd95e-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="dd95e-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="dd95e-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
