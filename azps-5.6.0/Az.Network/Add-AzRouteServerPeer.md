---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
ms.openlocfilehash: 430292ba3a387a0b2a0285b26c147c375f114398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979779"
---
# <span data-ttu-id="0acdd-101">Add-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="0acdd-101">Add-AzRouteServerPeer</span></span>

## <span data-ttu-id="0acdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0acdd-102">SYNOPSIS</span></span>
<span data-ttu-id="0acdd-103">Добавление одноранговых служб в Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="0acdd-103">Add a peer to an Azure RouteServer</span></span>

## <span data-ttu-id="0acdd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0acdd-104">SYNTAX</span></span>

### <span data-ttu-id="0acdd-105">RouteServerNPeerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0acdd-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0acdd-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0acdd-106">RouteServerNameParameterSet</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0acdd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0acdd-107">DESCRIPTION</span></span>
<span data-ttu-id="0acdd-108">**Cmdlet Add-AzRouteServerPeer добавляет** однорангового узла RouteServer в Azure RouteServer.</span><span class="sxs-lookup"><span data-stu-id="0acdd-108">The **Add-AzRouteServerPeer** cmdlet adds a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="0acdd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0acdd-109">EXAMPLES</span></span>

### <span data-ttu-id="0acdd-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0acdd-110">Example 1</span></span>
```powershell
PS C:\> Add-AzRouteServerPeer -ResourceGroupName $rgname -RouteServerName $routeServerName -PeerName $peerName -PeerIp "192.168.1.5" -PeerAsn "20000"
```

## <span data-ttu-id="0acdd-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0acdd-111">PARAMETERS</span></span>

### <span data-ttu-id="0acdd-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0acdd-112">-AsJob</span></span>
<span data-ttu-id="0acdd-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0acdd-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0acdd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0acdd-114">-DefaultProfile</span></span>
<span data-ttu-id="0acdd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0acdd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0acdd-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0acdd-116">-Force</span></span>
<span data-ttu-id="0acdd-117">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="0acdd-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0acdd-118">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="0acdd-118">-PeerAsn</span></span>
<span data-ttu-id="0acdd-119">ASN одноранговых серверов удаленных маршрутов.</span><span class="sxs-lookup"><span data-stu-id="0acdd-119">ASN of remote route server peer.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0acdd-120">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="0acdd-120">-PeerIp</span></span>
<span data-ttu-id="0acdd-121">Ip-адрес удаленного сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="0acdd-121">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="0acdd-122">-PeerName</span><span class="sxs-lookup"><span data-stu-id="0acdd-122">-PeerName</span></span>
<span data-ttu-id="0acdd-123">Имя одноранговых серверов маршрутов.</span><span class="sxs-lookup"><span data-stu-id="0acdd-123">The name of the route server peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0acdd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0acdd-124">-ResourceGroupName</span></span>
<span data-ttu-id="0acdd-125">Имя группы ресурсов сервера/одноранговой сети маршрутов.</span><span class="sxs-lookup"><span data-stu-id="0acdd-125">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="0acdd-126">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="0acdd-126">-RouteServerName</span></span>
<span data-ttu-id="0acdd-127">Сервер маршрутов, на котором имеется одноранговая серверная.</span><span class="sxs-lookup"><span data-stu-id="0acdd-127">The route server where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RouteServerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0acdd-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0acdd-128">-Confirm</span></span>
<span data-ttu-id="0acdd-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0acdd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0acdd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0acdd-130">-WhatIf</span></span>
<span data-ttu-id="0acdd-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0acdd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0acdd-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0acdd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0acdd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0acdd-133">CommonParameters</span></span>
<span data-ttu-id="0acdd-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0acdd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0acdd-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0acdd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0acdd-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0acdd-136">INPUTS</span></span>

### <span data-ttu-id="0acdd-137">System.String</span><span class="sxs-lookup"><span data-stu-id="0acdd-137">System.String</span></span>

### <span data-ttu-id="0acdd-138">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="0acdd-138">System.UInt32</span></span>

## <span data-ttu-id="0acdd-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0acdd-139">OUTPUTS</span></span>

### <span data-ttu-id="0acdd-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="0acdd-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="0acdd-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0acdd-141">NOTES</span></span>

## <span data-ttu-id="0acdd-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0acdd-142">RELATED LINKS</span></span>
