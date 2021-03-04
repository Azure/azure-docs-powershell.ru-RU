---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 22d2396e4471e2321ff9e532d4361909baa67163
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952019"
---
# <span data-ttu-id="8dc13-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dc13-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="8dc13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dc13-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc13-103">Обновляет виртуальный сетевой касание.</span><span class="sxs-lookup"><span data-stu-id="8dc13-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="8dc13-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8dc13-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc13-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dc13-105">DESCRIPTION</span></span>
<span data-ttu-id="8dc13-106">Командлет **Set-AzVirtualNetworkTap** обновляет виртуальный сетевой касание.</span><span class="sxs-lookup"><span data-stu-id="8dc13-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="8dc13-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8dc13-107">EXAMPLES</span></span>

### <span data-ttu-id="8dc13-108">Пример 1. Настройка виртуального сетевого касания</span><span class="sxs-lookup"><span data-stu-id="8dc13-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="8dc13-109">Команда обновляет назначение IpConfiguration и виртуальный сетевой касание.</span><span class="sxs-lookup"><span data-stu-id="8dc13-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="8dc13-110">Если на нее ссылаются конфигурации tap, после обновления весь исходный трафик не будет зеркально отражен в новой конфигурации IP-адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="8dc13-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="8dc13-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dc13-111">PARAMETERS</span></span>

### <span data-ttu-id="8dc13-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dc13-112">-AsJob</span></span>
<span data-ttu-id="8dc13-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8dc13-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8dc13-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc13-114">-DefaultProfile</span></span>
<span data-ttu-id="8dc13-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dc13-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dc13-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dc13-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="8dc13-117">Виртуальный сетевой касание</span><span class="sxs-lookup"><span data-stu-id="8dc13-117">The virtual network tap</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc13-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dc13-118">-Confirm</span></span>
<span data-ttu-id="8dc13-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dc13-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc13-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc13-120">-WhatIf</span></span>
<span data-ttu-id="8dc13-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dc13-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dc13-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8dc13-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc13-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc13-123">CommonParameters</span></span>
<span data-ttu-id="8dc13-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dc13-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc13-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dc13-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc13-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8dc13-126">INPUTS</span></span>

### <span data-ttu-id="8dc13-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dc13-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="8dc13-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8dc13-128">OUTPUTS</span></span>

### <span data-ttu-id="8dc13-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dc13-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="8dc13-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8dc13-130">NOTES</span></span>

## <span data-ttu-id="8dc13-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dc13-131">RELATED LINKS</span></span>

[<span data-ttu-id="8dc13-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dc13-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="8dc13-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dc13-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="8dc13-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8dc13-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
