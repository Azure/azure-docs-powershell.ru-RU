---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: 95a9e996612827b355b141165231651e17c78f6d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244517"
---
# <span data-ttu-id="a25e1-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="a25e1-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="a25e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a25e1-102">SYNOPSIS</span></span>
<span data-ttu-id="a25e1-103">Создает монитор SAP для указанной подписки, группы ресурсов и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="a25e1-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="a25e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a25e1-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a25e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a25e1-105">DESCRIPTION</span></span>
<span data-ttu-id="a25e1-106">Создает монитор SAP для указанной подписки, группы ресурсов и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="a25e1-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="a25e1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a25e1-107">EXAMPLES</span></span>

### <span data-ttu-id="a25e1-108">Пример 1: новый монитор SAP</span><span class="sxs-lookup"><span data-stu-id="a25e1-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="a25e1-109">Эта команда создает монитор SAP.</span><span class="sxs-lookup"><span data-stu-id="a25e1-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="a25e1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a25e1-110">PARAMETERS</span></span>

### <span data-ttu-id="a25e1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a25e1-111">-AsJob</span></span>
<span data-ttu-id="a25e1-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="a25e1-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a25e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a25e1-113">-DefaultProfile</span></span>
<span data-ttu-id="a25e1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a25e1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25e1-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="a25e1-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="a25e1-116">Значение, указывающее, следует ли отправлять аналитические данные в Майкрософт</span><span class="sxs-lookup"><span data-stu-id="a25e1-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="a25e1-117">-Location</span><span class="sxs-lookup"><span data-stu-id="a25e1-117">-Location</span></span>
<span data-ttu-id="a25e1-118">Географическое расположение, в котором находится ресурс</span><span class="sxs-lookup"><span data-stu-id="a25e1-118">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25e1-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="a25e1-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="a25e1-120">ИДЕНТИФИКАТОР рабочей области для службы анализа журналов, которая будет использоваться для наблюдения.</span><span class="sxs-lookup"><span data-stu-id="a25e1-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25e1-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="a25e1-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="a25e1-122">Идентификатор ARM рабочей области для анализа журналов, используемой для наблюдения</span><span class="sxs-lookup"><span data-stu-id="a25e1-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25e1-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="a25e1-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="a25e1-124">Общий ключ рабочей области для анализа журналов, используемой для наблюдения</span><span class="sxs-lookup"><span data-stu-id="a25e1-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25e1-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="a25e1-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="a25e1-126">Подсеть, в которой будет развернут монитор SAP.</span><span class="sxs-lookup"><span data-stu-id="a25e1-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="a25e1-127">Она должна находиться в одной подсети для базы данных HANA.</span><span class="sxs-lookup"><span data-stu-id="a25e1-127">It should be the same subnet of HANA database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25e1-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a25e1-128">-Name</span></span>
<span data-ttu-id="a25e1-129">Имя ресурса монитора SAP.</span><span class="sxs-lookup"><span data-stu-id="a25e1-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25e1-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="a25e1-130">-NoWait</span></span>
<span data-ttu-id="a25e1-131">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="a25e1-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a25e1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a25e1-132">-ResourceGroupName</span></span>
<span data-ttu-id="a25e1-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a25e1-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25e1-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a25e1-134">-SubscriptionId</span></span>
<span data-ttu-id="a25e1-135">Идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a25e1-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a25e1-136">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a25e1-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25e1-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="a25e1-137">-Tag</span></span>
<span data-ttu-id="a25e1-138">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a25e1-138">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25e1-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a25e1-139">-Confirm</span></span>
<span data-ttu-id="a25e1-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a25e1-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25e1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a25e1-141">-WhatIf</span></span>
<span data-ttu-id="a25e1-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a25e1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a25e1-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a25e1-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a25e1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a25e1-144">CommonParameters</span></span>
<span data-ttu-id="a25e1-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a25e1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a25e1-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a25e1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a25e1-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a25e1-147">INPUTS</span></span>

## <span data-ttu-id="a25e1-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a25e1-148">OUTPUTS</span></span>

### <span data-ttu-id="a25e1-149">Microsoft. Azure. PowerShell. командлеты. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="a25e1-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="a25e1-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="a25e1-150">NOTES</span></span>

<span data-ttu-id="a25e1-151">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a25e1-151">ALIASES</span></span>

## <span data-ttu-id="a25e1-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a25e1-152">RELATED LINKS</span></span>
