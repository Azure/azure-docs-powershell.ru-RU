---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 0c918328eb0b578eae31994c949210d62eba337b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563156"
---
# <span data-ttu-id="ff204-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ff204-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="ff204-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff204-102">SYNOPSIS</span></span>
<span data-ttu-id="ff204-103">Возвращает развертывание конфигурации узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="ff204-103">Gets DSC Node configuration deployments in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff204-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff204-104">SYNTAX</span></span>

### <span data-ttu-id="ff204-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff204-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff204-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="ff204-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff204-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff204-107">DESCRIPTION</span></span>
<span data-ttu-id="ff204-108">Командлет **Get-AzureRmAutomationDscNodeConfigurationDeployment** разворачивает конфигурацию узла AP Desired State Configuration (DSC) в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ff204-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="ff204-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff204-109">EXAMPLES</span></span>

### <span data-ttu-id="ff204-110">Пример 1: получение развертывания конфигурации узла</span><span class="sxs-lookup"><span data-stu-id="ff204-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="ff204-111">Приведенная выше команда развертывает конфигурацию узла DSC с именем "Config01. NODE1" в данном двухмерном многомерном массиве имен узлов.</span><span class="sxs-lookup"><span data-stu-id="ff204-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="ff204-112">Развертывание происходит поэтапным образом.</span><span class="sxs-lookup"><span data-stu-id="ff204-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="ff204-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff204-113">PARAMETERS</span></span>

### <span data-ttu-id="ff204-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ff204-114">-AutomationAccountName</span></span>
<span data-ttu-id="ff204-115">Указывает имя учетной записи автоматизации, содержащей конфигурацию DSC, которая компилируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="ff204-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="ff204-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff204-116">-DefaultProfile</span></span>
<span data-ttu-id="ff204-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ff204-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff204-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ff204-118">-EndTime</span></span>
<span data-ttu-id="ff204-119">Фильтр по времени окончания.</span><span class="sxs-lookup"><span data-stu-id="ff204-119">End time filter.</span></span>

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

### <span data-ttu-id="ff204-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="ff204-120">-JobId</span></span>
<span data-ttu-id="ff204-121">Указывает код задания для существующего задания развертывания.</span><span class="sxs-lookup"><span data-stu-id="ff204-121">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="ff204-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff204-122">-ResourceGroupName</span></span>
<span data-ttu-id="ff204-123">Указывает имя группы ресурсов, в которой этот командлет компилирует конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ff204-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="ff204-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ff204-124">-StartTime</span></span>
<span data-ttu-id="ff204-125">Начало фильтра времени начала.</span><span class="sxs-lookup"><span data-stu-id="ff204-125">Start time filter.</span></span>

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

### <span data-ttu-id="ff204-126">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="ff204-126">-Status</span></span>
<span data-ttu-id="ff204-127">Состояние фильтра заданий.</span><span class="sxs-lookup"><span data-stu-id="ff204-127">Status of the Job filter.</span></span>

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

### <span data-ttu-id="ff204-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff204-128">CommonParameters</span></span>
<span data-ttu-id="ff204-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff204-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff204-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff204-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff204-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff204-131">INPUTS</span></span>

### <span data-ttu-id="ff204-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ff204-132">System.Guid</span></span>

### <span data-ttu-id="ff204-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ff204-133">System.String</span></span>

## <span data-ttu-id="ff204-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff204-134">OUTPUTS</span></span>

### <span data-ttu-id="ff204-135">Microsoft. Azure. Commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ff204-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="ff204-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff204-136">NOTES</span></span>

## <span data-ttu-id="ff204-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff204-137">RELATED LINKS</span></span>

[<span data-ttu-id="ff204-138">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="ff204-138">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="ff204-139">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff204-139">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="ff204-140">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ff204-140">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="ff204-141">Остановить-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="ff204-141">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="ff204-142">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="ff204-142">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
