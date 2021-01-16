---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouterPeer.md
ms.openlocfilehash: 242a3985d75e0a741c5e2175c098139b448f3e70
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519866"
---
# <span data-ttu-id="8ccef-101">Update-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="8ccef-101">Update-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="8ccef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ccef-102">SYNOPSIS</span></span>
<span data-ttu-id="8ccef-103">Обновление одноранговой сети в Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="8ccef-103">Update a Peer in an Azure VirtualRouter</span></span>

## <span data-ttu-id="8ccef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ccef-104">SYNTAX</span></span>

### <span data-ttu-id="8ccef-105">VirtualRouterNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ccef-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ccef-106">VirtualRouterPeerNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ccef-106">VirtualRouterPeerNameParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ccef-107">VirtualRouterPeerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ccef-107">VirtualRouterPeerObjectParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String>
 -InputObject <PSVirtualRouterPeer> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ccef-108">VirtualRouterPeerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ccef-108">VirtualRouterPeerResourceIdParameterSet</span></span>
```
Update-AzVirtualRouterPeer -ResourceGroupName <String> -VirtualRouterName <String> -ResourceId <String>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ccef-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ccef-109">DESCRIPTION</span></span>
<span data-ttu-id="8ccef-110">С **его использованием** можно обновить одноранговую службу VirtualRouter до Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="8ccef-110">The **Update-AzVirtualRouterPeer** cmdlet updates a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="8ccef-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ccef-111">EXAMPLES</span></span>

### <span data-ttu-id="8ccef-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ccef-112">Example 1</span></span>
```powershell
Update-AzVirtualRouterPeer -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="8ccef-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8ccef-113">Example 2</span></span>
```powershell
$virtualRouterPeerId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/testVirtualRouter/peerings/csr'
Update-AzVirtualRouterPeer -ResourceId $virtualRouterPeerId  -VirtualRouterName virtualRouter -ResourceGroupName virtualRouterRG
```

### <span data-ttu-id="8ccef-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8ccef-114">Example 3</span></span>
```powershell
$virtualRouterPeer = Get-AzVirtualRouterPeer -ResourceGroupName testVirtualRouter -RouterName virtualRouter -PeerName csr
Update-AzVirtualRouterPeer -ResourceGroupName virtualRouterRG -InputObject $virtualRouterPeer  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="8ccef-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ccef-115">PARAMETERS</span></span>

### <span data-ttu-id="8ccef-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ccef-116">-AsJob</span></span>
<span data-ttu-id="8ccef-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8ccef-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ccef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ccef-118">-DefaultProfile</span></span>
<span data-ttu-id="8ccef-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ccef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ccef-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8ccef-120">-Force</span></span>
<span data-ttu-id="8ccef-121">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="8ccef-121">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8ccef-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ccef-122">-InputObject</span></span>
<span data-ttu-id="8ccef-123">Виртуальный объект ввода одноранговых маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="8ccef-123">The virtual router peer input object.</span></span>

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

### <span data-ttu-id="8ccef-124">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="8ccef-124">-PeerAsn</span></span>
<span data-ttu-id="8ccef-125">Одноранговая asn.</span><span class="sxs-lookup"><span data-stu-id="8ccef-125">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: VirtualRouterPeerNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ccef-126">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="8ccef-126">-PeerIp</span></span>
<span data-ttu-id="8ccef-127">Одноранговая ip-адрес.</span><span class="sxs-lookup"><span data-stu-id="8ccef-127">Peer Ip.</span></span>

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

### <span data-ttu-id="8ccef-128">-PeerName</span><span class="sxs-lookup"><span data-stu-id="8ccef-128">-PeerName</span></span>
<span data-ttu-id="8ccef-129">Имя виртуального одноранговых маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="8ccef-129">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="8ccef-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ccef-130">-ResourceGroupName</span></span>
<span data-ttu-id="8ccef-131">Имя группы ресурсов виртуального маршрутизатора или одноранговой сети.</span><span class="sxs-lookup"><span data-stu-id="8ccef-131">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="8ccef-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ccef-132">-ResourceId</span></span>
<span data-ttu-id="8ccef-133">ИД виртуального маршрутизатора-одноранговых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ccef-133">The virtual router peer resource Id.</span></span>

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

### <span data-ttu-id="8ccef-134">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="8ccef-134">-VirtualRouterName</span></span>
<span data-ttu-id="8ccef-135">Виртуальный маршрутизатор, в котором существует одноранговая компания.</span><span class="sxs-lookup"><span data-stu-id="8ccef-135">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="8ccef-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ccef-136">-Confirm</span></span>
<span data-ttu-id="8ccef-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ccef-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ccef-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ccef-138">-WhatIf</span></span>
<span data-ttu-id="8ccef-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ccef-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ccef-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8ccef-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ccef-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ccef-141">CommonParameters</span></span>
<span data-ttu-id="8ccef-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ccef-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ccef-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ccef-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ccef-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ccef-144">INPUTS</span></span>

### <span data-ttu-id="8ccef-145">System.String</span><span class="sxs-lookup"><span data-stu-id="8ccef-145">System.String</span></span>

### <span data-ttu-id="8ccef-146">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="8ccef-146">System.UInt32</span></span>

### <span data-ttu-id="8ccef-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="8ccef-147">Microsoft.Azure.Commands.Network.Models.PSVirtualRouterPeer</span></span>

## <span data-ttu-id="8ccef-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ccef-148">OUTPUTS</span></span>

### <span data-ttu-id="8ccef-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="8ccef-149">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="8ccef-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ccef-150">NOTES</span></span>

## <span data-ttu-id="8ccef-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ccef-151">RELATED LINKS</span></span>
