---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 99f76a12afdbc883d990fff5a05e06e2880aecf1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985886"
---
# <span data-ttu-id="27779-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="27779-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="27779-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27779-102">SYNOPSIS</span></span>
<span data-ttu-id="27779-103">Списки маршрутов, усвояемые определенным виртуальным маршрутизатором</span><span class="sxs-lookup"><span data-stu-id="27779-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="27779-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="27779-104">SYNTAX</span></span>

### <span data-ttu-id="27779-105">VirtualRouterPeerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27779-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27779-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27779-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27779-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27779-107">DESCRIPTION</span></span>
<span data-ttu-id="27779-108">Проуммировать маршруты, усвоимые виртуальным маршрутизатором из других источников.</span><span class="sxs-lookup"><span data-stu-id="27779-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="27779-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="27779-109">EXAMPLES</span></span>

### <span data-ttu-id="27779-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="27779-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="27779-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="27779-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="27779-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27779-112">PARAMETERS</span></span>

### <span data-ttu-id="27779-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27779-113">-AsJob</span></span>
<span data-ttu-id="27779-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="27779-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27779-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27779-115">-DefaultProfile</span></span>
<span data-ttu-id="27779-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27779-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27779-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27779-117">-InputObject</span></span>
<span data-ttu-id="27779-118">Виртуальный объект ввода одноранговых маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="27779-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="27779-119">-PeerName</span><span class="sxs-lookup"><span data-stu-id="27779-119">-PeerName</span></span>
<span data-ttu-id="27779-120">Имя виртуального маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="27779-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="27779-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27779-121">-ResourceGroupName</span></span>
<span data-ttu-id="27779-122">Имя группы виртуальных одноранговых ресурсов маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="27779-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="27779-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="27779-123">-VirtualRouterName</span></span>
<span data-ttu-id="27779-124">Имя виртуального маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="27779-124">Virtual router name</span></span>

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

### <span data-ttu-id="27779-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27779-125">CommonParameters</span></span>
<span data-ttu-id="27779-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27779-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27779-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27779-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27779-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27779-128">INPUTS</span></span>

### <span data-ttu-id="27779-129">System.String</span><span class="sxs-lookup"><span data-stu-id="27779-129">System.String</span></span>

### <span data-ttu-id="27779-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="27779-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="27779-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="27779-131">OUTPUTS</span></span>

### <span data-ttu-id="27779-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="27779-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="27779-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="27779-133">NOTES</span></span>

## <span data-ttu-id="27779-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27779-134">RELATED LINKS</span></span>
