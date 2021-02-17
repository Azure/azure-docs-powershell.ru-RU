---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azrouteserverpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzRouteServerPeer.md
ms.openlocfilehash: 70f7573a604ea15c33f1949883503fed2a356e00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226084"
---
# <span data-ttu-id="ccead-101">Add-AzRouteServerPeer</span><span class="sxs-lookup"><span data-stu-id="ccead-101">Add-AzRouteServerPeer</span></span>

## <span data-ttu-id="ccead-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccead-102">SYNOPSIS</span></span>
<span data-ttu-id="ccead-103">Добавление одноранговых служб в Azure RouteServer</span><span class="sxs-lookup"><span data-stu-id="ccead-103">Add a peer to an Azure RouteServer</span></span>

## <span data-ttu-id="ccead-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ccead-104">SYNTAX</span></span>

### <span data-ttu-id="ccead-105">RouteServerNPeerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ccead-105">RouteServerNPeerNameParameterSet (Default)</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccead-106">RouteServerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccead-106">RouteServerNameParameterSet</span></span>
```
Add-AzRouteServerPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -RouteServerName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ccead-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ccead-107">DESCRIPTION</span></span>
<span data-ttu-id="ccead-108">Для добавления однорангового узла RouteServer в Azure RouteServer можно добавить **cmdlet Add-AzRouteServerPeerer.**</span><span class="sxs-lookup"><span data-stu-id="ccead-108">The **Add-AzRouteServerPeer** cmdlet adds a RouteServer Peer to an Azure RouteServer</span></span>

## <span data-ttu-id="ccead-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ccead-109">EXAMPLES</span></span>

### <span data-ttu-id="ccead-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ccead-110">Example 1</span></span>
```powershell
PS C:\> Add-AzRouteServerPeer -ResourceGroupName $rgname -RouteServerName $routeServerName -PeerName $peerName -PeerIp "192.168.1.5" -PeerAsn "20000"
```

## <span data-ttu-id="ccead-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccead-111">PARAMETERS</span></span>

### <span data-ttu-id="ccead-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccead-112">-AsJob</span></span>
<span data-ttu-id="ccead-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ccead-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccead-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccead-114">-DefaultProfile</span></span>
<span data-ttu-id="ccead-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ccead-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccead-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ccead-116">-Force</span></span>
<span data-ttu-id="ccead-117">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="ccead-117">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ccead-118">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="ccead-118">-PeerAsn</span></span>
<span data-ttu-id="ccead-119">ASN одноранговых серверов удаленных маршрутов.</span><span class="sxs-lookup"><span data-stu-id="ccead-119">ASN of remote route server peer.</span></span>

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

### <span data-ttu-id="ccead-120">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="ccead-120">-PeerIp</span></span>
<span data-ttu-id="ccead-121">Ip-адрес удаленного сервера маршрутов.</span><span class="sxs-lookup"><span data-stu-id="ccead-121">Ip of remote route server peer.</span></span>

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

### <span data-ttu-id="ccead-122">-PeerName</span><span class="sxs-lookup"><span data-stu-id="ccead-122">-PeerName</span></span>
<span data-ttu-id="ccead-123">Имя одноранговых серверов маршрутов.</span><span class="sxs-lookup"><span data-stu-id="ccead-123">The name of the route server peer.</span></span>

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

### <span data-ttu-id="ccead-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccead-124">-ResourceGroupName</span></span>
<span data-ttu-id="ccead-125">Имя группы ресурсов сервера/одноранговой сети маршрутов.</span><span class="sxs-lookup"><span data-stu-id="ccead-125">The resource group name of the route server/peer.</span></span>

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

### <span data-ttu-id="ccead-126">-RouteServerName</span><span class="sxs-lookup"><span data-stu-id="ccead-126">-RouteServerName</span></span>
<span data-ttu-id="ccead-127">Сервер маршрутов, на котором имеется одноранговая серверная.</span><span class="sxs-lookup"><span data-stu-id="ccead-127">The route server where peer exists.</span></span>

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

### <span data-ttu-id="ccead-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ccead-128">-Confirm</span></span>
<span data-ttu-id="ccead-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ccead-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccead-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccead-130">-WhatIf</span></span>
<span data-ttu-id="ccead-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccead-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccead-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ccead-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccead-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccead-133">CommonParameters</span></span>
<span data-ttu-id="ccead-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccead-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccead-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ccead-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccead-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ccead-136">INPUTS</span></span>

### <span data-ttu-id="ccead-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ccead-137">System.String</span></span>

### <span data-ttu-id="ccead-138">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="ccead-138">System.UInt32</span></span>

## <span data-ttu-id="ccead-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ccead-139">OUTPUTS</span></span>

### <span data-ttu-id="ccead-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span><span class="sxs-lookup"><span data-stu-id="ccead-140">Microsoft.Azure.Commands.Network.Models.PSRouteServer</span></span>

## <span data-ttu-id="ccead-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ccead-141">NOTES</span></span>

## <span data-ttu-id="ccead-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ccead-142">RELATED LINKS</span></span>
