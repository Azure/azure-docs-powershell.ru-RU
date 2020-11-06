---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 1d767677c547c2418ca19e3206f3ca5a25638de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568864"
---
# <span data-ttu-id="d8c1e-101">Set-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d8c1e-101">Set-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="d8c1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c1e-103">Задает состояние цели для команды TAP для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d8c1e-103">Sets the goal state for a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8c1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8c1e-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8c1e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8c1e-105">DESCRIPTION</span></span>
<span data-ttu-id="d8c1e-106">**Set-AzureRmVirtualNetworkTap** задает состояние цели для команды TAP для виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="d8c1e-106">The **Set-AzureRmVirtualNetworkTap** sets the goal state for an Azure virtual network tap.</span></span>

## <span data-ttu-id="d8c1e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8c1e-107">EXAMPLES</span></span>

### <span data-ttu-id="d8c1e-108">Пример 1: Настройка TAP виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="d8c1e-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzureRmVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="d8c1e-109">Эта команда обновляет конечную конфигурацию и обновляет его нажатие.</span><span class="sxs-lookup"><span data-stu-id="d8c1e-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="d8c1e-110">Если есть какие-либо конфигурации касаний, которые ссылаются на него, то весь исходный трафик не будет зеркально отражен в новой конечной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d8c1e-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="d8c1e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8c1e-111">PARAMETERS</span></span>

### <span data-ttu-id="d8c1e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8c1e-112">-AsJob</span></span>
<span data-ttu-id="d8c1e-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d8c1e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8c1e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c1e-114">-DefaultProfile</span></span>
<span data-ttu-id="d8c1e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8c1e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c1e-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d8c1e-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="d8c1e-117">Нажмите виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="d8c1e-117">The virtual network tap</span></span>

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

### <span data-ttu-id="d8c1e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8c1e-118">-Confirm</span></span>
<span data-ttu-id="d8c1e-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d8c1e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8c1e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8c1e-120">-WhatIf</span></span>
<span data-ttu-id="d8c1e-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8c1e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8c1e-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8c1e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8c1e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8c1e-123">CommonParameters</span></span>
<span data-ttu-id="d8c1e-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8c1e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8c1e-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8c1e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8c1e-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8c1e-126">INPUTS</span></span>

### <span data-ttu-id="d8c1e-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d8c1e-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="d8c1e-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8c1e-128">OUTPUTS</span></span>

### <span data-ttu-id="d8c1e-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="d8c1e-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="d8c1e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8c1e-130">NOTES</span></span>

## <span data-ttu-id="d8c1e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8c1e-131">RELATED LINKS</span></span>
