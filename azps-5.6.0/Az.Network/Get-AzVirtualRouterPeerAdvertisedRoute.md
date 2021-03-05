---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouterpeeradvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerAdvertisedRoute.md
ms.openlocfilehash: aae01212b44eebf03207f2b0bfed788992acbc8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015075"
---
# <span data-ttu-id="01851-101">Get-AzVirtualRouterPeerAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="01851-101">Get-AzVirtualRouterPeerAdvertisedRoute</span></span>

## <span data-ttu-id="01851-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01851-102">SYNOPSIS</span></span>
<span data-ttu-id="01851-103">Списки маршрутов, объявленных определенным виртуальным маршрутизатором</span><span class="sxs-lookup"><span data-stu-id="01851-103">List routes being advertised by specific virtual router peer</span></span>

## <span data-ttu-id="01851-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="01851-104">SYNTAX</span></span>

### <span data-ttu-id="01851-105">VirtualRouterPeerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01851-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -ResourceGroupName <String> -VirtualRouterName <String>
 -PeerName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="01851-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="01851-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerAdvertisedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01851-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01851-107">DESCRIPTION</span></span>
<span data-ttu-id="01851-108">С учетом одноранговых виртуальных маршрутизаторов (по имени или по объекту) продумывка маршрутов, объявленных в этом пире с помощью определенного виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="01851-108">Given A virtual router peer either by name or by object, enumerate routes being advertised to that peer by a specific virtual router.</span></span>

## <span data-ttu-id="01851-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="01851-109">EXAMPLES</span></span>

### <span data-ttu-id="01851-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="01851-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerAdvertisedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="01851-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="01851-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerAdvertisedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="01851-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01851-112">PARAMETERS</span></span>

### <span data-ttu-id="01851-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01851-113">-AsJob</span></span>
<span data-ttu-id="01851-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="01851-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01851-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01851-115">-DefaultProfile</span></span>
<span data-ttu-id="01851-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01851-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01851-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01851-117">-InputObject</span></span>
<span data-ttu-id="01851-118">Виртуальный объект ввода одноранговых маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="01851-118">The virtual router peer input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01851-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="01851-119">-PeerName</span></span>
<span data-ttu-id="01851-120">Имя виртуального маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="01851-120">Virtual router peer name</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01851-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01851-121">-ResourceGroupName</span></span>
<span data-ttu-id="01851-122">Имя группы виртуальных одноранговых ресурсов маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="01851-122">Virtual router peer resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01851-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="01851-123">-VirtualRouterName</span></span>
<span data-ttu-id="01851-124">Имя виртуального маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="01851-124">Virtual router name</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01851-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01851-125">CommonParameters</span></span>
<span data-ttu-id="01851-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01851-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01851-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01851-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01851-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01851-128">INPUTS</span></span>

### <span data-ttu-id="01851-129">System.String</span><span class="sxs-lookup"><span data-stu-id="01851-129">System.String</span></span>

### <span data-ttu-id="01851-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="01851-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="01851-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="01851-131">OUTPUTS</span></span>

### <span data-ttu-id="01851-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="01851-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="01851-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="01851-133">NOTES</span></span>

## <span data-ttu-id="01851-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01851-134">RELATED LINKS</span></span>
