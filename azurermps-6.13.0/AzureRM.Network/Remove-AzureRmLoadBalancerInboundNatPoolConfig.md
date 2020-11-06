---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 6f9fd09aa87c8a812bf43a14068feb1604d8de8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556616"
---
# <span data-ttu-id="13043-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="13043-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="13043-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13043-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13043-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13043-103">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13043-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13043-104">DESCRIPTION</span></span>

## <span data-ttu-id="13043-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13043-105">EXAMPLES</span></span>

### <span data-ttu-id="13043-106">1: удаление</span><span class="sxs-lookup"><span data-stu-id="13043-106">1: Remove</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmLoadBalancerInboundNatPoolConfig -Name myinboundnatpool -LoadBalancer $slb
```

## <span data-ttu-id="13043-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13043-107">PARAMETERS</span></span>

### <span data-ttu-id="13043-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13043-108">-DefaultProfile</span></span>
<span data-ttu-id="13043-109">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13043-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13043-110">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="13043-110">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13043-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="13043-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13043-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13043-112">-Confirm</span></span>
<span data-ttu-id="13043-113">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="13043-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13043-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13043-114">-WhatIf</span></span>
<span data-ttu-id="13043-115">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="13043-115">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13043-116">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="13043-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13043-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13043-117">CommonParameters</span></span>
<span data-ttu-id="13043-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13043-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13043-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13043-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13043-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13043-120">INPUTS</span></span>

### <span data-ttu-id="13043-121">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="13043-121">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="13043-122">Параметры: подсистема балансировки (ByValue)</span><span class="sxs-lookup"><span data-stu-id="13043-122">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="13043-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13043-123">OUTPUTS</span></span>

### <span data-ttu-id="13043-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="13043-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="13043-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="13043-125">NOTES</span></span>

## <span data-ttu-id="13043-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13043-126">RELATED LINKS</span></span>
