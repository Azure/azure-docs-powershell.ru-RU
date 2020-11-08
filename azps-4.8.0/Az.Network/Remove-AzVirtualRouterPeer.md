---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235992"
---
# <span data-ttu-id="e1520-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="e1520-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="e1520-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1520-102">SYNOPSIS</span></span>
<span data-ttu-id="e1520-103">Удаляет одноранговый элемент из Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e1520-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="e1520-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1520-104">SYNTAX</span></span>

### <span data-ttu-id="e1520-105">VirtualRouterPeerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1520-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1520-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1520-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1520-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1520-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1520-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1520-108">DESCRIPTION</span></span>
<span data-ttu-id="e1520-109">Командлет **Remove-AzVirtualRouterPeer** удаляет одноранговый элемент VirtualRouter из Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e1520-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="e1520-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1520-110">EXAMPLES</span></span>

### <span data-ttu-id="e1520-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e1520-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="e1520-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e1520-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="e1520-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e1520-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="e1520-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1520-114">PARAMETERS</span></span>

### <span data-ttu-id="e1520-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1520-115">-AsJob</span></span>
<span data-ttu-id="e1520-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e1520-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1520-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1520-117">-DefaultProfile</span></span>
<span data-ttu-id="e1520-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1520-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1520-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e1520-119">-Force</span></span>
<span data-ttu-id="e1520-120">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="e1520-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e1520-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1520-121">-InputObject</span></span>
<span data-ttu-id="e1520-122">Входной объект однорангового узла виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="e1520-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="e1520-123">-Одноранговое</span><span class="sxs-lookup"><span data-stu-id="e1520-123">-PeerName</span></span>
<span data-ttu-id="e1520-124">Имя узла виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="e1520-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="e1520-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1520-125">-ResourceGroupName</span></span>
<span data-ttu-id="e1520-126">Имя группы ресурсов виртуального маршрутизатора или однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="e1520-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="e1520-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1520-127">-ResourceId</span></span>
<span data-ttu-id="e1520-128">Идентификатор однорангового ресурса виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="e1520-128">The virtual router peer resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterPeerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1520-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="e1520-129">-VirtualRouterName</span></span>
<span data-ttu-id="e1520-130">Виртуальный маршрутизатор, на котором находится одноранговый.</span><span class="sxs-lookup"><span data-stu-id="e1520-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="e1520-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1520-131">-Confirm</span></span>
<span data-ttu-id="e1520-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e1520-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1520-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1520-133">-WhatIf</span></span>
<span data-ttu-id="e1520-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e1520-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1520-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e1520-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1520-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1520-136">CommonParameters</span></span>
<span data-ttu-id="e1520-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1520-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1520-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1520-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1520-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1520-139">INPUTS</span></span>

### <span data-ttu-id="e1520-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e1520-140">System.String</span></span>

### <span data-ttu-id="e1520-141">Microsoft. Azure. Commands. Network. Models. PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="e1520-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="e1520-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1520-142">OUTPUTS</span></span>

### <span data-ttu-id="e1520-143">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="e1520-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="e1520-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1520-144">NOTES</span></span>

## <span data-ttu-id="e1520-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1520-145">RELATED LINKS</span></span>
