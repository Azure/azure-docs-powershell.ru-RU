---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 2c88ac8c0f3f089a4a26bf0e29ec855281e7f8c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005928"
---
# <span data-ttu-id="eae86-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="eae86-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="eae86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eae86-102">SYNOPSIS</span></span>
<span data-ttu-id="eae86-103">Удаляет одноранг из Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="eae86-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="eae86-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eae86-104">SYNTAX</span></span>

### <span data-ttu-id="eae86-105">VirtualRouterPeerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eae86-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eae86-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eae86-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eae86-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eae86-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eae86-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eae86-108">DESCRIPTION</span></span>
<span data-ttu-id="eae86-109">Для удаления однорангового узла VirtualRouter из Azure VirtualRouter удаляется cmdlet **Remove-AzVirtualRouterPeer.**</span><span class="sxs-lookup"><span data-stu-id="eae86-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="eae86-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eae86-110">EXAMPLES</span></span>

### <span data-ttu-id="eae86-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eae86-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="eae86-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="eae86-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="eae86-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="eae86-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="eae86-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eae86-114">PARAMETERS</span></span>

### <span data-ttu-id="eae86-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eae86-115">-AsJob</span></span>
<span data-ttu-id="eae86-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="eae86-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eae86-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eae86-117">-DefaultProfile</span></span>
<span data-ttu-id="eae86-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eae86-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eae86-119">-Force</span><span class="sxs-lookup"><span data-stu-id="eae86-119">-Force</span></span>
<span data-ttu-id="eae86-120">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="eae86-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="eae86-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eae86-121">-InputObject</span></span>
<span data-ttu-id="eae86-122">Виртуальный объект ввода одноранговых маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="eae86-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="eae86-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="eae86-123">-PeerName</span></span>
<span data-ttu-id="eae86-124">Имя виртуального одноранговых маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="eae86-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="eae86-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eae86-125">-ResourceGroupName</span></span>
<span data-ttu-id="eae86-126">Имя группы ресурсов виртуального маршрутизатора или одноранговой сети.</span><span class="sxs-lookup"><span data-stu-id="eae86-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="eae86-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eae86-127">-ResourceId</span></span>
<span data-ttu-id="eae86-128">ИД виртуального маршрутизатора-одноранговых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eae86-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="eae86-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="eae86-129">-VirtualRouterName</span></span>
<span data-ttu-id="eae86-130">Виртуальный маршрутизатор, в котором существует одноранговая компания.</span><span class="sxs-lookup"><span data-stu-id="eae86-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="eae86-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eae86-131">-Confirm</span></span>
<span data-ttu-id="eae86-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="eae86-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eae86-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eae86-133">-WhatIf</span></span>
<span data-ttu-id="eae86-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eae86-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eae86-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eae86-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eae86-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eae86-136">CommonParameters</span></span>
<span data-ttu-id="eae86-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eae86-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eae86-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eae86-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eae86-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eae86-139">INPUTS</span></span>

### <span data-ttu-id="eae86-140">System.String</span><span class="sxs-lookup"><span data-stu-id="eae86-140">System.String</span></span>

### <span data-ttu-id="eae86-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="eae86-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="eae86-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eae86-142">OUTPUTS</span></span>

### <span data-ttu-id="eae86-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="eae86-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="eae86-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eae86-144">NOTES</span></span>

## <span data-ttu-id="eae86-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eae86-145">RELATED LINKS</span></span>
