---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1b51b7d086af738e356d7a6b65c17bdb45cbb518
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911847"
---
# <span data-ttu-id="9070c-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9070c-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="9070c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9070c-102">SYNOPSIS</span></span>
<span data-ttu-id="9070c-103">Создает ресурс TapConfiguration, связанный с NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="9070c-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="9070c-104">Это будет ссылаться на существующий ресурс VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="9070c-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="9070c-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9070c-105">SYNTAX</span></span>

### <span data-ttu-id="9070c-106">SetByResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9070c-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9070c-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9070c-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9070c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9070c-108">DESCRIPTION</span></span>
<span data-ttu-id="9070c-109">Командлет **Add-AzNetworkInterfaceTapConfig** создает ресурс TapConfiguration, связанный с NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="9070c-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="9070c-110">Это будет ссылаться на существующий ресурс VirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="9070c-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="9070c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9070c-111">EXAMPLES</span></span>

### <span data-ttu-id="9070c-112">Пример 1: Добавление TapConfiguration в заданный NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9070c-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="9070c-113">Добавьте TapConfiguration в sourceNic.</span><span class="sxs-lookup"><span data-stu-id="9070c-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="9070c-114">Трафик из VM sourceNic будет зеркально отображен на целевую виртуальную машину, на которую ссылается vVirtualNetworkTap ресурс.</span><span class="sxs-lookup"><span data-stu-id="9070c-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="9070c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9070c-115">PARAMETERS</span></span>

### <span data-ttu-id="9070c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9070c-116">-DefaultProfile</span></span>
<span data-ttu-id="9070c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9070c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9070c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9070c-118">-Name</span></span>
<span data-ttu-id="9070c-119">Имя конфигурации TAP.</span><span class="sxs-lookup"><span data-stu-id="9070c-119">Name of the tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9070c-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9070c-120">-NetworkInterface</span></span>
<span data-ttu-id="9070c-121">Ссылка на ресурс сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9070c-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9070c-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9070c-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="9070c-123">Ссылка на ресурс касания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9070c-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9070c-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="9070c-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="9070c-125">Ссылка на ресурс касания виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9070c-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9070c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9070c-126">-Confirm</span></span>
<span data-ttu-id="9070c-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9070c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9070c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9070c-128">-WhatIf</span></span>
<span data-ttu-id="9070c-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9070c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9070c-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9070c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9070c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9070c-131">CommonParameters</span></span>
<span data-ttu-id="9070c-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9070c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9070c-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9070c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9070c-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9070c-134">INPUTS</span></span>

### <span data-ttu-id="9070c-135">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9070c-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="9070c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9070c-136">System.String</span></span>

### <span data-ttu-id="9070c-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="9070c-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="9070c-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9070c-138">OUTPUTS</span></span>

### <span data-ttu-id="9070c-139">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9070c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="9070c-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="9070c-140">NOTES</span></span>

## <span data-ttu-id="9070c-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9070c-141">RELATED LINKS</span></span>

[<span data-ttu-id="9070c-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9070c-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="9070c-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9070c-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="9070c-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="9070c-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
