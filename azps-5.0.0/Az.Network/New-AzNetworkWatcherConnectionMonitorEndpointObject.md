---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316644"
---
# <span data-ttu-id="2858b-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="2858b-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="2858b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2858b-102">SYNOPSIS</span></span>
<span data-ttu-id="2858b-103">Создание конечной точки монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="2858b-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="2858b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2858b-104">SYNTAX</span></span>

### <span data-ttu-id="2858b-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="2858b-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2858b-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="2858b-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2858b-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="2858b-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2858b-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="2858b-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2858b-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="2858b-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2858b-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="2858b-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2858b-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2858b-111">DESCRIPTION</span></span>
<span data-ttu-id="2858b-112">New-AzNetworkWatcherConnectionMonitorEndpointObject командлет создает конечную точку монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="2858b-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="2858b-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2858b-113">EXAMPLES</span></span>

### <span data-ttu-id="2858b-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2858b-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="2858b-115">Name (имя): workspaceEndpoint тип: MMAWorkspaceMachine ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace адрес: scope: {"include": [{"адрес": "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="2858b-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="2858b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2858b-116">PARAMETERS</span></span>

### <span data-ttu-id="2858b-117">-Address (адрес)</span><span class="sxs-lookup"><span data-stu-id="2858b-117">-Address</span></span>
<span data-ttu-id="2858b-118">Адрес конечной точки монитора соединений (IP или доменное имя).</span><span class="sxs-lookup"><span data-stu-id="2858b-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExternalAddress, MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2858b-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="2858b-119">-AzureSubnet</span></span>
<span data-ttu-id="2858b-120">Переключатель конечной точки подсети Azure.</span><span class="sxs-lookup"><span data-stu-id="2858b-120">Azure Subnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2858b-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="2858b-121">-AzureVM</span></span>
<span data-ttu-id="2858b-122">Коммутатор конечной точки виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="2858b-122">Azure VM endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2858b-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="2858b-123">-AzureVNet</span></span>
<span data-ttu-id="2858b-124">Коммутатор конечной точки Azure vnet.</span><span class="sxs-lookup"><span data-stu-id="2858b-124">Azure Vnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVNet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2858b-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="2858b-125">-CoverageLevel</span></span>
<span data-ttu-id="2858b-126">Тестовое покрытие для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2858b-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="2858b-127">Поддерживаются значения по умолчанию, Low, BelowAverage, Average, AboveAvergae, Full.</span><span class="sxs-lookup"><span data-stu-id="2858b-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2858b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2858b-128">-DefaultProfile</span></span>
<span data-ttu-id="2858b-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2858b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2858b-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="2858b-130">-ExcludeItem</span></span>
<span data-ttu-id="2858b-131">Список элементов, которые необходимо исключить из области конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2858b-131">List of items which need to be excluded from endpoint scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2858b-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="2858b-132">-ExternalAddress</span></span>
<span data-ttu-id="2858b-133">Ключ конечной точки внешнего адреса.</span><span class="sxs-lookup"><span data-stu-id="2858b-133">External Address endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExternalAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2858b-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="2858b-134">-IncludeItem</span></span>
<span data-ttu-id="2858b-135">Список элементов, которые необходимо включить в область endpont.</span><span class="sxs-lookup"><span data-stu-id="2858b-135">List of items which need to be included into endpont scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, MMAWorkspaceMachine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2858b-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="2858b-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="2858b-137">Переключатель конечной точки компьютера рабочей области MMA.</span><span class="sxs-lookup"><span data-stu-id="2858b-137">MMA Workspace Machine endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2858b-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="2858b-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="2858b-139">Переключатель конечной точки сети MMA рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2858b-139">MMA Workspace Network endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2858b-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2858b-140">-Name</span></span>
<span data-ttu-id="2858b-141">Имя конечной точки монитора соединений.</span><span class="sxs-lookup"><span data-stu-id="2858b-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="2858b-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2858b-142">-ResourceId</span></span>
<span data-ttu-id="2858b-143">Идентификатор ресурса конечной точки монитора соединений.</span><span class="sxs-lookup"><span data-stu-id="2858b-143">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM, AzureVNet, AzureSubnet, MMAWorkspaceMachine, MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2858b-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2858b-144">-Confirm</span></span>
<span data-ttu-id="2858b-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2858b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2858b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2858b-146">-WhatIf</span></span>
<span data-ttu-id="2858b-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2858b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2858b-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2858b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2858b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2858b-149">CommonParameters</span></span>
<span data-ttu-id="2858b-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2858b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2858b-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2858b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2858b-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2858b-152">INPUTS</span></span>

### <span data-ttu-id="2858b-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="2858b-153">None</span></span>

## <span data-ttu-id="2858b-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2858b-154">OUTPUTS</span></span>

### <span data-ttu-id="2858b-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="2858b-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="2858b-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="2858b-156">NOTES</span></span>

## <span data-ttu-id="2858b-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2858b-157">RELATED LINKS</span></span>
