---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouterpeerlearnedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouterPeerLearnedRoute.md
ms.openlocfilehash: 8c01f935196cb5aaaf553d1c1041589def80aeeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246901"
---
# <span data-ttu-id="aa06c-101">Get-AzVirtualRouterPeerLearnedRoute</span><span class="sxs-lookup"><span data-stu-id="aa06c-101">Get-AzVirtualRouterPeerLearnedRoute</span></span>

## <span data-ttu-id="aa06c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa06c-102">SYNOPSIS</span></span>
<span data-ttu-id="aa06c-103">Маршруты списков, полученные определенным одноранговым узлом виртуального маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="aa06c-103">List routes learned by a specific virtual router peer</span></span>

## <span data-ttu-id="aa06c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa06c-104">SYNTAX</span></span>

### <span data-ttu-id="aa06c-105">VirtualRouterPeerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa06c-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -ResourceGroupName <String> -VirtualRouterName <String> -PeerName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa06c-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa06c-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Get-AzVirtualRouterPeerLearnedRoute -InputObject <PSVirtualRouterPeer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa06c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa06c-107">DESCRIPTION</span></span>
<span data-ttu-id="aa06c-108">Перечисление маршрутов, полученных одноранговым узлом виртуального маршрутизатора, из других источников.</span><span class="sxs-lookup"><span data-stu-id="aa06c-108">Enumerate routes learned by a virtual router peer from other sources.</span></span>

## <span data-ttu-id="aa06c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa06c-109">EXAMPLES</span></span>

### <span data-ttu-id="aa06c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa06c-110">Example 1</span></span>
```powershell
Get-AzVirtualRouterPeerLearnedRouter -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
```

### <span data-ttu-id="aa06c-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="aa06c-111">Example 2</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName $resourceGroupName -VirtualRouterName $virtualRouterName -PeerName $peerName
Get-AzVirtualRouterPeerLearnedRouter -InputObject $virtualRouterPeer
```

## <span data-ttu-id="aa06c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa06c-112">PARAMETERS</span></span>

### <span data-ttu-id="aa06c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa06c-113">-AsJob</span></span>
<span data-ttu-id="aa06c-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aa06c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa06c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa06c-115">-DefaultProfile</span></span>
<span data-ttu-id="aa06c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa06c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa06c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa06c-117">-InputObject</span></span>
<span data-ttu-id="aa06c-118">Входной объект однорангового узла виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="aa06c-118">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="aa06c-119">-Одноранговое</span><span class="sxs-lookup"><span data-stu-id="aa06c-119">-PeerName</span></span>
<span data-ttu-id="aa06c-120">Имя однорангового узла виртуального маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="aa06c-120">Virtual router peer name</span></span>

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

### <span data-ttu-id="aa06c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa06c-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa06c-122">Имя группы ресурсов однорангового узла виртуального маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="aa06c-122">Virtual router peer resource group's name</span></span>

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

### <span data-ttu-id="aa06c-123">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="aa06c-123">-VirtualRouterName</span></span>
<span data-ttu-id="aa06c-124">Имя виртуального маршрутизатора</span><span class="sxs-lookup"><span data-stu-id="aa06c-124">Virtual router name</span></span>

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

### <span data-ttu-id="aa06c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa06c-125">CommonParameters</span></span>
<span data-ttu-id="aa06c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa06c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa06c-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa06c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa06c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa06c-128">INPUTS</span></span>

### <span data-ttu-id="aa06c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="aa06c-129">System.String</span></span>

### <span data-ttu-id="aa06c-130">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="aa06c-130">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="aa06c-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa06c-131">OUTPUTS</span></span>

### <span data-ttu-id="aa06c-132">Microsoft. Azure. Commands. Network. Models. PSPeerRoute</span><span class="sxs-lookup"><span data-stu-id="aa06c-132">Microsoft.Azure.Commands.Network.Models.PSPeerRoute</span></span>

## <span data-ttu-id="aa06c-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa06c-133">NOTES</span></span>

## <span data-ttu-id="aa06c-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa06c-134">RELATED LINKS</span></span>
