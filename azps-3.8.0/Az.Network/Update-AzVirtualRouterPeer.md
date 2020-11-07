---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 8d7bbf361ee2fc2bf06e1bf3ce6a9bfe1e295338
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912953"
---
# <span data-ttu-id="99313-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="99313-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="99313-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99313-102">SYNOPSIS</span></span>
<span data-ttu-id="99313-103">Обновление однорангового элемента в Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="99313-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="99313-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99313-104">SYNTAX</span></span>

### <span data-ttu-id="99313-105">VirtualRouterNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="99313-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99313-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="99313-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99313-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99313-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99313-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99313-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99313-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99313-109">DESCRIPTION</span></span>
<span data-ttu-id="99313-110">Командлет **Update-AzVirtualRouterPeer** обновляет одноранговый узел VirtualRouter до Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="99313-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="99313-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99313-111">EXAMPLES</span></span>

### <span data-ttu-id="99313-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="99313-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="99313-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="99313-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="99313-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="99313-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="99313-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99313-115">PARAMETERS</span></span>

### <span data-ttu-id="99313-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99313-116">-AsJob</span></span>
<span data-ttu-id="99313-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="99313-117">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99313-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99313-118">-DefaultProfile</span></span>
<span data-ttu-id="99313-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99313-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99313-120">-Force</span><span class="sxs-lookup"><span data-stu-id="99313-120">-Force</span></span>
<span data-ttu-id="99313-121">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="99313-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99313-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99313-122">-InputObject</span></span>
<span data-ttu-id="99313-123">Входной объект однорангового узла виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="99313-123">The virtual router peer input object.</span></span>

```yaml
Type: PSVirtualRouterPeer
Parameter Sets: VirtualRouterPeerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99313-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="99313-124">-PeerAsn</span></span>
<span data-ttu-id="99313-125">Одноранговый ASN.</span><span class="sxs-lookup"><span data-stu-id="99313-125">Peer ASN.</span></span>

```yaml
Type: UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99313-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="99313-126">-PeerIp</span></span>
<span data-ttu-id="99313-127">Одноранговый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="99313-127">Peer Ip.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99313-128">-Одноранговое</span><span class="sxs-lookup"><span data-stu-id="99313-128">-PeerName</span></span>
<span data-ttu-id="99313-129">Имя узла виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="99313-129">The name of the virtual router Peer.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99313-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99313-130">-ResourceGroupName</span></span>
<span data-ttu-id="99313-131">Имя группы ресурсов виртуального маршрутизатора или однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="99313-131">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99313-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99313-132">-ResourceId</span></span>
<span data-ttu-id="99313-133">Идентификатор однорангового ресурса виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="99313-133">The virtual router peer resource Id.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99313-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="99313-134">-VirtualRouterName</span></span>
<span data-ttu-id="99313-135">Виртуальный маршрутизатор, на котором находится одноранговый.</span><span class="sxs-lookup"><span data-stu-id="99313-135">The virtual router where peer exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99313-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99313-136">-Confirm</span></span>
<span data-ttu-id="99313-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="99313-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99313-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99313-138">-WhatIf</span></span>
<span data-ttu-id="99313-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="99313-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99313-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="99313-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99313-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99313-141">CommonParameters</span></span>
<span data-ttu-id="99313-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99313-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99313-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99313-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99313-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99313-144">INPUTS</span></span>

### <span data-ttu-id="99313-145">System. String</span><span class="sxs-lookup"><span data-stu-id="99313-145">System.String</span></span>

### <span data-ttu-id="99313-146">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="99313-146">System.UInt32</span></span>

### <span data-ttu-id="99313-147">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="99313-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="99313-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99313-148">OUTPUTS</span></span>

### <span data-ttu-id="99313-149">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="99313-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="99313-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="99313-150">NOTES</span></span>

## <span data-ttu-id="99313-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99313-151">RELATED LINKS</span></span>
