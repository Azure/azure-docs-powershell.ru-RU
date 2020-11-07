---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 5a68c17f26109f5000e82d31e21e0f0330b7c87a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904350"
---
# <span data-ttu-id="84cab-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="84cab-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="84cab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84cab-102">SYNOPSIS</span></span>
<span data-ttu-id="84cab-103">Обновляет виртуальную сетевую команду TAP.</span><span class="sxs-lookup"><span data-stu-id="84cab-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="84cab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84cab-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84cab-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84cab-105">DESCRIPTION</span></span>
<span data-ttu-id="84cab-106">Командлет **Set-AzVirtualNetworkTap** обновляет виртуальную сетевую команду TAP.</span><span class="sxs-lookup"><span data-stu-id="84cab-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="84cab-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84cab-107">EXAMPLES</span></span>

### <span data-ttu-id="84cab-108">Пример 1: Настройка TAP виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="84cab-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="84cab-109">Эта команда обновляет конечную конфигурацию и обновляет его нажатие.</span><span class="sxs-lookup"><span data-stu-id="84cab-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="84cab-110">Если есть какие-либо конфигурации касаний, которые ссылаются на него, то весь исходный трафик не будет зеркально отражен в новой конечной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="84cab-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="84cab-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84cab-111">PARAMETERS</span></span>

### <span data-ttu-id="84cab-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84cab-112">-AsJob</span></span>
<span data-ttu-id="84cab-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="84cab-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84cab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84cab-114">-DefaultProfile</span></span>
<span data-ttu-id="84cab-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84cab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84cab-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="84cab-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="84cab-117">Нажмите виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="84cab-117">The virtual network tap</span></span>

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

### <span data-ttu-id="84cab-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84cab-118">-Confirm</span></span>
<span data-ttu-id="84cab-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84cab-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84cab-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84cab-120">-WhatIf</span></span>
<span data-ttu-id="84cab-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="84cab-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84cab-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="84cab-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84cab-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84cab-123">CommonParameters</span></span>
<span data-ttu-id="84cab-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84cab-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84cab-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84cab-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84cab-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84cab-126">INPUTS</span></span>

### <span data-ttu-id="84cab-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="84cab-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="84cab-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84cab-128">OUTPUTS</span></span>

### <span data-ttu-id="84cab-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="84cab-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="84cab-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="84cab-130">NOTES</span></span>

## <span data-ttu-id="84cab-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84cab-131">RELATED LINKS</span></span>

[<span data-ttu-id="84cab-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="84cab-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="84cab-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="84cab-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="84cab-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="84cab-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
