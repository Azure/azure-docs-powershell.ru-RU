---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 58e26de74abb46234f6985c3973b5bbe494bd0ad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234988"
---
# <span data-ttu-id="daa54-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="daa54-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="daa54-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="daa54-102">SYNOPSIS</span></span>
<span data-ttu-id="daa54-103">Создание конечной точки монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="daa54-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="daa54-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="daa54-104">SYNTAX</span></span>

### <span data-ttu-id="daa54-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="daa54-105">SetByResourceId</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] -ResourceId <String>
 [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="daa54-106">SetByAddress</span><span class="sxs-lookup"><span data-stu-id="daa54-106">SetByAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] [-Address <String>] [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daa54-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="daa54-107">DESCRIPTION</span></span>
<span data-ttu-id="daa54-108">New-AzNetworkWatcherConnectionMonitorEndpointObject командлет создает конечную точку монитора подключений.</span><span class="sxs-lookup"><span data-stu-id="daa54-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="daa54-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="daa54-109">EXAMPLES</span></span>

### <span data-ttu-id="daa54-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="daa54-110">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name "workspaceEndpoint" -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

<span data-ttu-id="daa54-111">Name (имя): workspaceEndpoint ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace адрес: Filter: {"Type": "include", "Items": [{"тип": "AgentAddress"; "адрес": "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="daa54-111">Name       : workspaceEndpoint ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Filter     : { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="daa54-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="daa54-112">PARAMETERS</span></span>

### <span data-ttu-id="daa54-113">-Address (адрес)</span><span class="sxs-lookup"><span data-stu-id="daa54-113">-Address</span></span>
<span data-ttu-id="daa54-114">Адрес конечной точки монитора соединений (IP или доменное имя).</span><span class="sxs-lookup"><span data-stu-id="daa54-114">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa54-115">-DefaultProfile</span></span>
<span data-ttu-id="daa54-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="daa54-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daa54-117">-FilterItem</span><span class="sxs-lookup"><span data-stu-id="daa54-117">-FilterItem</span></span>
<span data-ttu-id="daa54-118">Список элементов в фильтре.</span><span class="sxs-lookup"><span data-stu-id="daa54-118">List of items in the filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa54-119">-FilterType</span><span class="sxs-lookup"><span data-stu-id="daa54-119">-FilterType</span></span>
<span data-ttu-id="daa54-120">Поведение фильтра конечной точки.</span><span class="sxs-lookup"><span data-stu-id="daa54-120">The behavior of the endpoint filter.</span></span> <span data-ttu-id="daa54-121">В настоящее время поддерживается только функция include.</span><span class="sxs-lookup"><span data-stu-id="daa54-121">Currently only 'Include' is supported.</span></span>

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

### <span data-ttu-id="daa54-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="daa54-122">-Name</span></span>
<span data-ttu-id="daa54-123">Имя конечной точки монитора соединений.</span><span class="sxs-lookup"><span data-stu-id="daa54-123">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="daa54-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="daa54-124">-ResourceId</span></span>
<span data-ttu-id="daa54-125">Идентификатор ресурса конечной точки монитора соединений.</span><span class="sxs-lookup"><span data-stu-id="daa54-125">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa54-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="daa54-126">-Confirm</span></span>
<span data-ttu-id="daa54-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="daa54-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daa54-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daa54-128">-WhatIf</span></span>
<span data-ttu-id="daa54-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="daa54-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daa54-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="daa54-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daa54-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa54-131">CommonParameters</span></span>
<span data-ttu-id="daa54-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="daa54-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa54-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="daa54-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa54-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="daa54-134">INPUTS</span></span>

### <span data-ttu-id="daa54-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="daa54-135">None</span></span>

## <span data-ttu-id="daa54-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="daa54-136">OUTPUTS</span></span>

### <span data-ttu-id="daa54-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="daa54-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="daa54-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="daa54-138">NOTES</span></span>

## <span data-ttu-id="daa54-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="daa54-139">RELATED LINKS</span></span>
