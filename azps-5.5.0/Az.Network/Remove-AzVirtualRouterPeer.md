---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouterPeer.md
ms.openlocfilehash: 147689b38f18caa1aa39ccd72d478e912336ad2b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240608"
---
# <span data-ttu-id="bd20f-101">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="bd20f-101">Remove-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="bd20f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd20f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd20f-103">Удаляет одноранг из Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="bd20f-103">Removes a Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="bd20f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd20f-104">SYNTAX</span></span>

### <span data-ttu-id="bd20f-105">VirtualRouterPeerNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd20f-105">VirtualRouterPeerNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -VirtualRouterName <String> [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd20f-106">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd20f-106">VirtualRouterPeerObjectParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd20f-107">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd20f-107">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouterPeer -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd20f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd20f-108">DESCRIPTION</span></span>
<span data-ttu-id="bd20f-109">Для удаления однорангового узла VirtualRouter из Azure VirtualRouter удаляется cmdlet **Remove-AzVirtualRouterPeer.**</span><span class="sxs-lookup"><span data-stu-id="bd20f-109">The **Remove-AzVirtualRouterPeer** cmdlet removes a VirtualRouter Peer from an Azure VirtualRouter</span></span>

## <span data-ttu-id="bd20f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd20f-110">EXAMPLES</span></span>

### <span data-ttu-id="bd20f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd20f-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouterPeer -PeerName csr -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="bd20f-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bd20f-112">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter/peerings/csr'
Remove-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId
```

### <span data-ttu-id="bd20f-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bd20f-113">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName virtualRouter -RouterName virtualRouter -PeerName csr
Remove-AzVirtualRouterPeer -InputObject $virtualRouterPeer
```

## <span data-ttu-id="bd20f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd20f-114">PARAMETERS</span></span>

### <span data-ttu-id="bd20f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd20f-115">-AsJob</span></span>
<span data-ttu-id="bd20f-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bd20f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd20f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd20f-117">-DefaultProfile</span></span>
<span data-ttu-id="bd20f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd20f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd20f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="bd20f-119">-Force</span></span>
<span data-ttu-id="bd20f-120">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="bd20f-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bd20f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd20f-121">-InputObject</span></span>
<span data-ttu-id="bd20f-122">Виртуальный объект ввода одноранговых маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="bd20f-122">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="bd20f-123">-PeerName</span><span class="sxs-lookup"><span data-stu-id="bd20f-123">-PeerName</span></span>
<span data-ttu-id="bd20f-124">Имя виртуального одноранговых маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="bd20f-124">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="bd20f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd20f-125">-ResourceGroupName</span></span>
<span data-ttu-id="bd20f-126">Имя группы ресурсов виртуального маршрутизатора или одноранговой сети.</span><span class="sxs-lookup"><span data-stu-id="bd20f-126">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="bd20f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd20f-127">-ResourceId</span></span>
<span data-ttu-id="bd20f-128">Виртуальный маршрутизатор с одноранговой инициалами ресурса.</span><span class="sxs-lookup"><span data-stu-id="bd20f-128">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="bd20f-129">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="bd20f-129">-VirtualRouterName</span></span>
<span data-ttu-id="bd20f-130">Виртуальный маршрутизатор, в котором существует одноранговая компания.</span><span class="sxs-lookup"><span data-stu-id="bd20f-130">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="bd20f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd20f-131">-Confirm</span></span>
<span data-ttu-id="bd20f-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd20f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd20f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd20f-133">-WhatIf</span></span>
<span data-ttu-id="bd20f-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd20f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd20f-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bd20f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd20f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd20f-136">CommonParameters</span></span>
<span data-ttu-id="bd20f-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd20f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd20f-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd20f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd20f-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd20f-139">INPUTS</span></span>

### <span data-ttu-id="bd20f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="bd20f-140">System.String</span></span>

### <span data-ttu-id="bd20f-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="bd20f-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="bd20f-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd20f-142">OUTPUTS</span></span>

### <span data-ttu-id="bd20f-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="bd20f-143">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="bd20f-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd20f-144">NOTES</span></span>

## <span data-ttu-id="bd20f-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd20f-145">RELATED LINKS</span></span>
