---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: 95a9e996612827b355b141165231651e17c78f6d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399708"
---
# <span data-ttu-id="b9232-101">New-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="b9232-101">New-AzSapMonitor</span></span>

## <span data-ttu-id="b9232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9232-102">SYNOPSIS</span></span>
<span data-ttu-id="b9232-103">Создает монитор SAP для указанной подписки, группы ресурсов и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="b9232-103">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="b9232-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b9232-104">SYNTAX</span></span>

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b9232-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9232-105">DESCRIPTION</span></span>
<span data-ttu-id="b9232-106">Создает монитор SAP для указанной подписки, группы ресурсов и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="b9232-106">Creates a SAP monitor for the specified subscription, resource group, and resource name.</span></span>

## <span data-ttu-id="b9232-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b9232-107">EXAMPLES</span></span>

### <span data-ttu-id="b9232-108">Пример 1. Новый монитор SAP</span><span class="sxs-lookup"><span data-stu-id="b9232-108">Example 1: New SAP monitor</span></span> 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="b9232-109">Эта команда создает монитор SAP.</span><span class="sxs-lookup"><span data-stu-id="b9232-109">This command creates a SAP monitor.</span></span>

## <span data-ttu-id="b9232-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9232-110">PARAMETERS</span></span>

### <span data-ttu-id="b9232-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9232-111">-AsJob</span></span>
<span data-ttu-id="b9232-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="b9232-112">Run the command as a job</span></span>

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

### <span data-ttu-id="b9232-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9232-113">-DefaultProfile</span></span>
<span data-ttu-id="b9232-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9232-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9232-115">-EnableCustomerAnalytic</span><span class="sxs-lookup"><span data-stu-id="b9232-115">-EnableCustomerAnalytic</span></span>
<span data-ttu-id="b9232-116">Значение, указывающее, следует ли отправлять аналитику в корпорацию Майкрософт</span><span class="sxs-lookup"><span data-stu-id="b9232-116">The value indicating whether to send analytics to Microsoft</span></span>

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

### <span data-ttu-id="b9232-117">-Location</span><span class="sxs-lookup"><span data-stu-id="b9232-117">-Location</span></span>
<span data-ttu-id="b9232-118">Географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="b9232-118">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="b9232-119">-LogAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="b9232-119">-LogAnalyticsWorkspaceId</span></span>
<span data-ttu-id="b9232-120">ИД рабочей области для анализа журнала, используемого для мониторинга</span><span class="sxs-lookup"><span data-stu-id="b9232-120">The workspace ID of the log analytics workspace to be used for monitoring</span></span>

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

### <span data-ttu-id="b9232-121">-LogAnalyticsWorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="b9232-121">-LogAnalyticsWorkspaceResourceId</span></span>
<span data-ttu-id="b9232-122">ARM ИД рабочей области аналитики журналов, используемой для мониторинга</span><span class="sxs-lookup"><span data-stu-id="b9232-122">The ARM ID of the Log Analytics Workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="b9232-123">-LogAnalyticsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="b9232-123">-LogAnalyticsWorkspaceSharedKey</span></span>
<span data-ttu-id="b9232-124">Общий ключ рабочей области аналитики журнала, используемой для мониторинга</span><span class="sxs-lookup"><span data-stu-id="b9232-124">The shared key of the log analytics workspace that is used for monitoring</span></span>

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

### <span data-ttu-id="b9232-125">-MonitorSubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="b9232-125">-MonitorSubnetResourceId</span></span>
<span data-ttu-id="b9232-126">Подсеть, в которой будет развернут монитор SAP.</span><span class="sxs-lookup"><span data-stu-id="b9232-126">The subnet which the SAP monitor will be deployed in.</span></span>
<span data-ttu-id="b9232-127">Это должна быть та же подсеть базы данных HANA.</span><span class="sxs-lookup"><span data-stu-id="b9232-127">It should be the same subnet of HANA database.</span></span>

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

### <span data-ttu-id="b9232-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b9232-128">-Name</span></span>
<span data-ttu-id="b9232-129">Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="b9232-129">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="b9232-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b9232-130">-NoWait</span></span>
<span data-ttu-id="b9232-131">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="b9232-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b9232-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9232-132">-ResourceGroupName</span></span>
<span data-ttu-id="b9232-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9232-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="b9232-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9232-134">-SubscriptionId</span></span>
<span data-ttu-id="b9232-135">ИД подписки, однозначно определяемой подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b9232-135">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b9232-136">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b9232-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b9232-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="b9232-137">-Tag</span></span>
<span data-ttu-id="b9232-138">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9232-138">Resource tags.</span></span>

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

### <span data-ttu-id="b9232-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9232-139">-Confirm</span></span>
<span data-ttu-id="b9232-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b9232-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9232-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9232-141">-WhatIf</span></span>
<span data-ttu-id="b9232-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9232-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9232-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b9232-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9232-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9232-144">CommonParameters</span></span>
<span data-ttu-id="b9232-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9232-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9232-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9232-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9232-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9232-147">INPUTS</span></span>

## <span data-ttu-id="b9232-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9232-148">OUTPUTS</span></span>

### <span data-ttu-id="b9232-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="b9232-149">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="b9232-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b9232-150">NOTES</span></span>

<span data-ttu-id="b9232-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b9232-151">ALIASES</span></span>

## <span data-ttu-id="b9232-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9232-152">RELATED LINKS</span></span>

