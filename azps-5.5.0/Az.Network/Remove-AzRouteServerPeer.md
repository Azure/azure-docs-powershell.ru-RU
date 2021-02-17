---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteServerPeer.md
ms.openlocfilehash: d177c0dfa5ff59fde0adfe8ac4e3598ae70127f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236561"
---
# <span data-ttu-id="59fa8-101">Remove-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="59fa8-101">Remove-AzRouteServerPeer</span></span>

## <span data-ttu-id="59fa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="59fa8-103">Удаляет одноранг из Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="59fa8-103">Removes a Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="59fa8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="59fa8-104">SYNTAX</span></span>

### <span data-ttu-id="59fa8-105">RouteServerNPeerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59fa8-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Remove-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -RouteServerName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59fa8-106">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59fa8-106">RouteServerNPeerInputObjectParameterSet</span></span>
```
Remove-AzRouteServerPeer -InputObject <PSRouteServerPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59fa8-107">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59fa8-107">RouteServerNPeerResourceIdParameterSet</span></span>
```
Remove-AzRouteServerPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59fa8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59fa8-108">DESCRIPTION</span></span>
<span data-ttu-id="59fa8-109">Для удаления однорангового узла RouteServer из Azure RouteServer удаляется cmdlet **Remove-AzRouteServerPeerer**</span><span class="sxs-lookup"><span data-stu-id="59fa8-109">The **Remove-AzRouteServerPeer** cmdlet removes a RouteServer Peer from an Azure RouteServer</span></span>

## <span data-ttu-id="59fa8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="59fa8-110">EXAMPLES</span></span>

### <span data-ttu-id="59fa8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59fa8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzRouteServerPeer -PeerName peer -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="59fa8-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="59fa8-112">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/peer'
Remove-AzRouteServerPeer -ResourceId $RouteServerPeerId
```

### <span data-ttu-id="59fa8-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="59fa8-113">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServerRG -RouteServerName routeServer -PeerName peer
Remove-AzRouteServerPeer -InputObject $RouteServerPeer
```
## <span data-ttu-id="59fa8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59fa8-114">PARAMETERS</span></span>

### <span data-ttu-id="59fa8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59fa8-115">-AsJob</span></span>
<span data-ttu-id="59fa8-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="59fa8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59fa8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59fa8-117">-DefaultProfile</span></span>
<span data-ttu-id="59fa8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59fa8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59fa8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="59fa8-119">-Force</span></span>
<span data-ttu-id="59fa8-120">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="59fa8-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="59fa8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59fa8-121">-InputObject</span></span>
<span data-ttu-id="59fa8-122">Объект ввода одноранговых серверов маршрутов.</span><span class="sxs-lookup"><span data-stu-id="59fa8-122">The route server peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer
Parameter Sets: RouteServerNPeerInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59fa8-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="59fa8-123">-PeerName</span></span>
<span data-ttu-id="59fa8-124">Имя одноранговых серверов маршрутов.</span><span class="sxs-lookup"><span data-stu-id="59fa8-124">The name of the route server Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59fa8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59fa8-125">-ResourceGroupName</span></span>
<span data-ttu-id="59fa8-126">Имя группы ресурсов сервера/одноранговой сети маршрутов.</span><span class="sxs-lookup"><span data-stu-id="59fa8-126">The resource group name of the route server/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59fa8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59fa8-127">-ResourceId</span></span>
<span data-ttu-id="59fa8-128">ИД ресурса одноранговых ресурсов сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="59fa8-128">The route server peer resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59fa8-129">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="59fa8-129">-RouteServerName</span></span>
<span data-ttu-id="59fa8-130">Сервер маршрутов, на котором имеется одноранговая серверная.</span><span class="sxs-lookup"><span data-stu-id="59fa8-130">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59fa8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59fa8-131">-Confirm</span></span>
<span data-ttu-id="59fa8-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="59fa8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59fa8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59fa8-133">-WhatIf</span></span>
<span data-ttu-id="59fa8-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59fa8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59fa8-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="59fa8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59fa8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59fa8-136">CommonParameters</span></span>
<span data-ttu-id="59fa8-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59fa8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59fa8-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59fa8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59fa8-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59fa8-139">INPUTS</span></span>

### <span data-ttu-id="59fa8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="59fa8-140">System.String</span></span>

### <span data-ttu-id="59fa8-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="59fa8-141">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="59fa8-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="59fa8-142">OUTPUTS</span></span>

### <span data-ttu-id="59fa8-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="59fa8-143">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="59fa8-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="59fa8-144">NOTES</span></span>

## <span data-ttu-id="59fa8-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59fa8-145">RELATED LINKS</span></span>
