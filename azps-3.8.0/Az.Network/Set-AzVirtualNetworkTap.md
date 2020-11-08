---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065122"
---
# <span data-ttu-id="5593a-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5593a-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="5593a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5593a-102">SYNOPSIS</span></span>
<span data-ttu-id="5593a-103">Обновляет виртуальную сетевую команду TAP.</span><span class="sxs-lookup"><span data-stu-id="5593a-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="5593a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5593a-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5593a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5593a-105">DESCRIPTION</span></span>
<span data-ttu-id="5593a-106">Командлет **Set-AzVirtualNetworkTap** обновляет виртуальную сетевую команду TAP.</span><span class="sxs-lookup"><span data-stu-id="5593a-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="5593a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5593a-107">EXAMPLES</span></span>

### <span data-ttu-id="5593a-108">Пример 1: Настройка TAP виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="5593a-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="5593a-109">Эта команда обновляет конечную конфигурацию и обновляет его нажатие.</span><span class="sxs-lookup"><span data-stu-id="5593a-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="5593a-110">Если есть какие-либо конфигурации касаний, которые ссылаются на него, то весь исходный трафик не будет зеркально отражен в новой конечной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5593a-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="5593a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5593a-111">PARAMETERS</span></span>

### <span data-ttu-id="5593a-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5593a-112">-AsJob</span></span>
<span data-ttu-id="5593a-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5593a-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5593a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5593a-114">-DefaultProfile</span></span>
<span data-ttu-id="5593a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5593a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5593a-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5593a-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="5593a-117">Нажмите виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="5593a-117">The virtual network tap</span></span>

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

### <span data-ttu-id="5593a-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5593a-118">-Confirm</span></span>
<span data-ttu-id="5593a-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5593a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5593a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5593a-120">-WhatIf</span></span>
<span data-ttu-id="5593a-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5593a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5593a-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5593a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5593a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5593a-123">CommonParameters</span></span>
<span data-ttu-id="5593a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5593a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5593a-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5593a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5593a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5593a-126">INPUTS</span></span>

### <span data-ttu-id="5593a-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5593a-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="5593a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5593a-128">OUTPUTS</span></span>

### <span data-ttu-id="5593a-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5593a-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="5593a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5593a-130">NOTES</span></span>

## <span data-ttu-id="5593a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5593a-131">RELATED LINKS</span></span>

[<span data-ttu-id="5593a-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5593a-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="5593a-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5593a-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="5593a-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="5593a-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
