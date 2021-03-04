---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzRouteServerPeer.md
ms.openlocfilehash: 3c0be49a09758648bcd2301f2643577ea8dcd951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951608"
---
# <span data-ttu-id="7ed9a-101">Update-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="7ed9a-101">Update-AzRouteServerPeer</span></span>

## <span data-ttu-id="7ed9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ed9a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ed9a-103">Обновление одноранговой сети в Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="7ed9a-103">Update a Peer in an Azure RouteServer</span></span>

## <span data-ttu-id="7ed9a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7ed9a-104">SYNTAX</span></span>

### <span data-ttu-id="7ed9a-105">RouteServerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7ed9a-105">RouteServerNameParameterSet (Default)</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ed9a-106">RouteServerNPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ed9a-106">RouteServerNPeerNameParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ed9a-107">RouteServerNPeerInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ed9a-107">RouteServerNPeerInputObjectParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -InputObject <PSRouteServerPeer>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ed9a-108">RouteServerNPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ed9a-108">RouteServerNPeerResourceIdParameterSet</span></span>
```
Update-AzRouteServerPeer -ResourceGroupName <String> -RouteServerName <String> -ResourceId <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ed9a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ed9a-109">DESCRIPTION</span></span>
<span data-ttu-id="7ed9a-110">Для **обновления azRouteServerPeer** одноранговых служб RouteServer обновляется до Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-110">The **Update-AzRouteServerPeer** cmdlet updates a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="7ed9a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7ed9a-111">EXAMPLES</span></span>

### <span data-ttu-id="7ed9a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7ed9a-112">Example 1</span></span>
```powershell
PS C:\> Update-AzRouteServerPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="7ed9a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7ed9a-113">Example 2</span></span>
```powershell
PS C:\> $routeServerPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/routeServerRG/providers/Microsoft.Network/virtualHubs/routeServer/bgpConnections/csr'
Update-AzRouteServerPeer -ResourceId $routeServerPeerId  -RouteServerName routeServer -ResourceGroupName routeServerRG
```

### <span data-ttu-id="7ed9a-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7ed9a-114">Example 3</span></span>
```powershell
PS C:\> $routeServerPeer = Get-AzRouteServerPeer -ResourceGroupName routeServer -RouteServerName routeServer -PeerName csr
Update-AzRouteServerPeer -ResourceGroupName routeServerRG -InputObject $routeServerPeer  -RouteServerName routeServer
```

## <span data-ttu-id="7ed9a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ed9a-115">PARAMETERS</span></span>

### <span data-ttu-id="7ed9a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ed9a-116">-AsJob</span></span>
<span data-ttu-id="7ed9a-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7ed9a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ed9a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ed9a-118">-DefaultProfile</span></span>
<span data-ttu-id="7ed9a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ed9a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7ed9a-120">-Force</span></span>
<span data-ttu-id="7ed9a-121">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="7ed9a-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7ed9a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ed9a-122">-InputObject</span></span>
<span data-ttu-id="7ed9a-123">Объект ввода одноранговых серверов маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-123">The route server peer input object.</span></span>

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

### <span data-ttu-id="7ed9a-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="7ed9a-124">-PeerAsn</span></span>
<span data-ttu-id="7ed9a-125">ASN одноранговых серверов удаленных маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-125">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: RouteServerNPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed9a-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="7ed9a-126">-PeerIp</span></span>
<span data-ttu-id="7ed9a-127">Ip-адрес удаленного сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-127">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="7ed9a-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="7ed9a-128">-PeerName</span></span>
<span data-ttu-id="7ed9a-129">Имя одноранговых серверов маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-129">The name of the route server Peer.</span></span>

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

### <span data-ttu-id="7ed9a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ed9a-130">-ResourceGroupName</span></span>
<span data-ttu-id="7ed9a-131">Имя группы ресурсов сервера/одноранговой сети маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-131">The resource group name of the route server/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed9a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7ed9a-132">-ResourceId</span></span>
<span data-ttu-id="7ed9a-133">ИД ресурса одноранговых ресурсов сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-133">The route server peer resource Id.</span></span>

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

### <span data-ttu-id="7ed9a-134">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="7ed9a-134">-RouteServerName</span></span>
<span data-ttu-id="7ed9a-135">Сервер маршрутов, на котором имеется одноранговая серверная.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-135">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ed9a-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ed9a-136">-Confirm</span></span>
<span data-ttu-id="7ed9a-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ed9a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ed9a-138">-WhatIf</span></span>
<span data-ttu-id="7ed9a-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ed9a-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ed9a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ed9a-141">CommonParameters</span></span>
<span data-ttu-id="7ed9a-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ed9a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ed9a-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ed9a-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ed9a-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ed9a-144">INPUTS</span></span>

### <span data-ttu-id="7ed9a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="7ed9a-145">System.String</span></span>

### <span data-ttu-id="7ed9a-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="7ed9a-146">System.UInt32</span></span>

### <span data-ttu-id="7ed9a-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="7ed9a-147">Microsoft.Azure.Commands.Network.Models.PSRouteServerPeer</span></span>

## <span data-ttu-id="7ed9a-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7ed9a-148">OUTPUTS</span></span>

### <span data-ttu-id="7ed9a-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="7ed9a-149">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="7ed9a-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7ed9a-150">NOTES</span></span>

## <span data-ttu-id="7ed9a-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ed9a-151">RELATED LINKS</span></span>
