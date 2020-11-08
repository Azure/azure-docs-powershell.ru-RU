---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 2cb7bc759847af456286bfc611904922a26dc443
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248850"
---
# <span data-ttu-id="377f4-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="377f4-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="377f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="377f4-102">SYNOPSIS</span></span>
<span data-ttu-id="377f4-103">Добавление однорангового узла в Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="377f4-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="377f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="377f4-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="377f4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="377f4-105">DESCRIPTION</span></span>
<span data-ttu-id="377f4-106">Командлет **Add-AzVirtualRouterPeer** добавляет одноранговый элемент VirtualRouter в Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="377f4-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="377f4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="377f4-107">EXAMPLES</span></span>

### <span data-ttu-id="377f4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="377f4-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="377f4-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="377f4-109">PARAMETERS</span></span>

### <span data-ttu-id="377f4-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="377f4-110">-AsJob</span></span>
<span data-ttu-id="377f4-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="377f4-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="377f4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="377f4-112">-DefaultProfile</span></span>
<span data-ttu-id="377f4-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="377f4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="377f4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="377f4-114">-Force</span></span>
<span data-ttu-id="377f4-115">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="377f4-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="377f4-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="377f4-116">-PeerAsn</span></span>
<span data-ttu-id="377f4-117">Одноранговый ASN.</span><span class="sxs-lookup"><span data-stu-id="377f4-117">Peer ASN.</span></span>

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

### <span data-ttu-id="377f4-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="377f4-118">-PeerIp</span></span>
<span data-ttu-id="377f4-119">Одноранговый IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="377f4-119">Peer Ip.</span></span>

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

### <span data-ttu-id="377f4-120">-Одноранговое</span><span class="sxs-lookup"><span data-stu-id="377f4-120">-PeerName</span></span>
<span data-ttu-id="377f4-121">Имя узла виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="377f4-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="377f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="377f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="377f4-123">Имя группы ресурсов виртуального маршрутизатора или однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="377f4-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="377f4-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="377f4-124">-VirtualRouterName</span></span>
<span data-ttu-id="377f4-125">Виртуальный маршрутизатор, на котором находится одноранговый.</span><span class="sxs-lookup"><span data-stu-id="377f4-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="377f4-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="377f4-126">-Confirm</span></span>
<span data-ttu-id="377f4-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="377f4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="377f4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="377f4-128">-WhatIf</span></span>
<span data-ttu-id="377f4-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="377f4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="377f4-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="377f4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="377f4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="377f4-131">CommonParameters</span></span>
<span data-ttu-id="377f4-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="377f4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="377f4-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="377f4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="377f4-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="377f4-134">INPUTS</span></span>

### <span data-ttu-id="377f4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="377f4-135">System.String</span></span>

### <span data-ttu-id="377f4-136">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="377f4-136">System.UInt32</span></span>

## <span data-ttu-id="377f4-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="377f4-137">OUTPUTS</span></span>

### <span data-ttu-id="377f4-138">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="377f4-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="377f4-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="377f4-139">NOTES</span></span>

## <span data-ttu-id="377f4-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="377f4-140">RELATED LINKS</span></span>
