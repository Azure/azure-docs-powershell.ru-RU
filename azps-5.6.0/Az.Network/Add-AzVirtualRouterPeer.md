---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 87647d504d47bf3f53b775d68b42ab617485f73d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979720"
---
# <span data-ttu-id="afb91-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="afb91-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="afb91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afb91-102">SYNOPSIS</span></span>
<span data-ttu-id="afb91-103">Добавление одноранговой сети в Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="afb91-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="afb91-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="afb91-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afb91-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afb91-105">DESCRIPTION</span></span>
<span data-ttu-id="afb91-106">**Cmdlet Add-AzVirtualRouterPeer** добавляет одноранг virtualRouter в Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="afb91-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="afb91-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="afb91-107">EXAMPLES</span></span>

### <span data-ttu-id="afb91-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="afb91-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="afb91-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afb91-109">PARAMETERS</span></span>

### <span data-ttu-id="afb91-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afb91-110">-AsJob</span></span>
<span data-ttu-id="afb91-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="afb91-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afb91-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb91-112">-DefaultProfile</span></span>
<span data-ttu-id="afb91-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afb91-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb91-114">-Force</span><span class="sxs-lookup"><span data-stu-id="afb91-114">-Force</span></span>
<span data-ttu-id="afb91-115">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="afb91-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="afb91-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="afb91-116">-PeerAsn</span></span>
<span data-ttu-id="afb91-117">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="afb91-117">Peer ASN.</span></span>

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

### <span data-ttu-id="afb91-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="afb91-118">-PeerIp</span></span>
<span data-ttu-id="afb91-119">Одноранговая ip-адрес.</span><span class="sxs-lookup"><span data-stu-id="afb91-119">Peer Ip.</span></span>

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

### <span data-ttu-id="afb91-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="afb91-120">-PeerName</span></span>
<span data-ttu-id="afb91-121">Имя виртуального одноранговых маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="afb91-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="afb91-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afb91-122">-ResourceGroupName</span></span>
<span data-ttu-id="afb91-123">Имя группы ресурсов виртуального маршрутизатора или одноранговой сети.</span><span class="sxs-lookup"><span data-stu-id="afb91-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="afb91-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="afb91-124">-VirtualRouterName</span></span>
<span data-ttu-id="afb91-125">Виртуальный маршрутизатор, в котором существует одноранговая компания.</span><span class="sxs-lookup"><span data-stu-id="afb91-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="afb91-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afb91-126">-Confirm</span></span>
<span data-ttu-id="afb91-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afb91-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb91-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afb91-128">-WhatIf</span></span>
<span data-ttu-id="afb91-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afb91-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afb91-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="afb91-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb91-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb91-131">CommonParameters</span></span>
<span data-ttu-id="afb91-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb91-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb91-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afb91-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb91-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afb91-134">INPUTS</span></span>

### <span data-ttu-id="afb91-135">System.String</span><span class="sxs-lookup"><span data-stu-id="afb91-135">System.String</span></span>

### <span data-ttu-id="afb91-136">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="afb91-136">System.UInt32</span></span>

## <span data-ttu-id="afb91-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="afb91-137">OUTPUTS</span></span>

### <span data-ttu-id="afb91-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="afb91-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="afb91-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="afb91-139">NOTES</span></span>

## <span data-ttu-id="afb91-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afb91-140">RELATED LINKS</span></span>
