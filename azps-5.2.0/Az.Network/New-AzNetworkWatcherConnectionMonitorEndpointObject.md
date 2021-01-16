---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394103"
---
# <span data-ttu-id="36dc9-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="36dc9-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="36dc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="36dc9-103">Создает конечную точку монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="36dc9-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="36dc9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36dc9-104">SYNTAX</span></span>

### <span data-ttu-id="36dc9-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="36dc9-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36dc9-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="36dc9-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36dc9-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="36dc9-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36dc9-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="36dc9-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36dc9-109">ЯЗРАБрабова</span><span class="sxs-lookup"><span data-stu-id="36dc9-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36dc9-110">ЯЗ.WorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="36dc9-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36dc9-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36dc9-111">DESCRIPTION</span></span>
<span data-ttu-id="36dc9-112">New-AzNetworkWatcherConnectionMonitorEndpointObject создает конечную точку монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="36dc9-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="36dc9-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36dc9-113">EXAMPLES</span></span>

### <span data-ttu-id="36dc9-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36dc9-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="36dc9-115">Name : workspaceEndpoint Type : WORKWorkspaceMachine ResourceId : /subscriptions/0000000-0000-0000-0000-0000-0000000000 resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address: Scope : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span><span class="sxs-lookup"><span data-stu-id="36dc9-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="36dc9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36dc9-116">PARAMETERS</span></span>

### <span data-ttu-id="36dc9-117">-Address</span><span class="sxs-lookup"><span data-stu-id="36dc9-117">-Address</span></span>
<span data-ttu-id="36dc9-118">Адрес конечной точки монитора подключения (IP или доменное имя).</span><span class="sxs-lookup"><span data-stu-id="36dc9-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

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

### <span data-ttu-id="36dc9-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="36dc9-119">-AzureSubnet</span></span>
<span data-ttu-id="36dc9-120">Переключатель конечных точек подсети Azure.</span><span class="sxs-lookup"><span data-stu-id="36dc9-120">Azure Subnet endpoint switch.</span></span>

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

### <span data-ttu-id="36dc9-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="36dc9-121">-AzureVM</span></span>
<span data-ttu-id="36dc9-122">Переключатель конечных точек Azure VM.</span><span class="sxs-lookup"><span data-stu-id="36dc9-122">Azure VM endpoint switch.</span></span>

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

### <span data-ttu-id="36dc9-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="36dc9-123">-AzureVNet</span></span>
<span data-ttu-id="36dc9-124">Переключатель конечных точек Azure Vnet.</span><span class="sxs-lookup"><span data-stu-id="36dc9-124">Azure Vnet endpoint switch.</span></span>

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

### <span data-ttu-id="36dc9-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="36dc9-125">-CoverageLevel</span></span>
<span data-ttu-id="36dc9-126">Тестовая покрытие для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="36dc9-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="36dc9-127">Поддерживаются значения по умолчанию, низкая, BelowAverage, Average, AboveAvergae, Full.</span><span class="sxs-lookup"><span data-stu-id="36dc9-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

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

### <span data-ttu-id="36dc9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36dc9-128">-DefaultProfile</span></span>
<span data-ttu-id="36dc9-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36dc9-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36dc9-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="36dc9-130">-ExcludeItem</span></span>
<span data-ttu-id="36dc9-131">Список элементов, которые необходимо исключить из области действия конечной точки.</span><span class="sxs-lookup"><span data-stu-id="36dc9-131">List of items which need to be excluded from endpoint scope.</span></span>

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

### <span data-ttu-id="36dc9-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="36dc9-132">-ExternalAddress</span></span>
<span data-ttu-id="36dc9-133">Переключатель внешней конечной точки адреса.</span><span class="sxs-lookup"><span data-stu-id="36dc9-133">External Address endpoint switch.</span></span>

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

### <span data-ttu-id="36dc9-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="36dc9-134">-IncludeItem</span></span>
<span data-ttu-id="36dc9-135">Список элементов, которые необходимо включить в область действия endpont.</span><span class="sxs-lookup"><span data-stu-id="36dc9-135">List of items which need to be included into endpont scope.</span></span>

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

### <span data-ttu-id="36dc9-136">-WORKWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="36dc9-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="36dc9-137">Переключатель конечной точки компьютера рабочей области ЕАО.</span><span class="sxs-lookup"><span data-stu-id="36dc9-137">MMA Workspace Machine endpoint switch.</span></span>

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

### <span data-ttu-id="36dc9-138">-WORKWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="36dc9-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="36dc9-139">Переключатель конечной точки сети рабочей области рабочей области ЕАО.</span><span class="sxs-lookup"><span data-stu-id="36dc9-139">MMA Workspace Network endpoint switch.</span></span>

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

### <span data-ttu-id="36dc9-140">-Name</span><span class="sxs-lookup"><span data-stu-id="36dc9-140">-Name</span></span>
<span data-ttu-id="36dc9-141">Имя конечной точки монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="36dc9-141">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="36dc9-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36dc9-142">-ResourceId</span></span>
<span data-ttu-id="36dc9-143">ИД ресурса конечной точки монитора подключения.</span><span class="sxs-lookup"><span data-stu-id="36dc9-143">Resource ID of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="36dc9-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36dc9-144">-Confirm</span></span>
<span data-ttu-id="36dc9-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36dc9-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36dc9-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36dc9-146">-WhatIf</span></span>
<span data-ttu-id="36dc9-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36dc9-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36dc9-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="36dc9-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36dc9-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36dc9-149">CommonParameters</span></span>
<span data-ttu-id="36dc9-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36dc9-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36dc9-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36dc9-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36dc9-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36dc9-152">INPUTS</span></span>

### <span data-ttu-id="36dc9-153">Нет</span><span class="sxs-lookup"><span data-stu-id="36dc9-153">None</span></span>

## <span data-ttu-id="36dc9-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36dc9-154">OUTPUTS</span></span>

### <span data-ttu-id="36dc9-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="36dc9-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="36dc9-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36dc9-156">NOTES</span></span>

## <span data-ttu-id="36dc9-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36dc9-157">RELATED LINKS</span></span>
