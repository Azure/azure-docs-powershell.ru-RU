---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 010fd83d8b8e26e67e35afcc54b03ca0c1a5bd5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072980"
---
# <span data-ttu-id="48b5e-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="48b5e-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="48b5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48b5e-102">SYNOPSIS</span></span>
<span data-ttu-id="48b5e-103">Создание коллекции правил NAT для политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="48b5e-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="48b5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48b5e-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48b5e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48b5e-105">DESCRIPTION</span></span>
<span data-ttu-id="48b5e-106">Командлет **New-AzFirewallPolicyNatRuleCollection** создает семейство правил NAT для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="48b5e-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="48b5e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48b5e-107">EXAMPLES</span></span>

### <span data-ttu-id="48b5e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="48b5e-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="48b5e-109">В этом примере создается набор правил NAT с сетевым правилом</span><span class="sxs-lookup"><span data-stu-id="48b5e-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="48b5e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48b5e-110">PARAMETERS</span></span>

### <span data-ttu-id="48b5e-111">-Себя</span><span class="sxs-lookup"><span data-stu-id="48b5e-111">-ActionType</span></span>
<span data-ttu-id="48b5e-112">Тип действия правила.</span><span class="sxs-lookup"><span data-stu-id="48b5e-112">The type of the rule action</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Dnat

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b5e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b5e-113">-DefaultProfile</span></span>
<span data-ttu-id="48b5e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48b5e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b5e-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="48b5e-115">-Name</span></span>
<span data-ttu-id="48b5e-116">Имя коллекции сетевых правил</span><span class="sxs-lookup"><span data-stu-id="48b5e-116">The name of the Network Rule Collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b5e-117">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="48b5e-117">-Priority</span></span>
<span data-ttu-id="48b5e-118">Приоритет коллекции правил</span><span class="sxs-lookup"><span data-stu-id="48b5e-118">The priority of the rule collection</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b5e-119">-Правило</span><span class="sxs-lookup"><span data-stu-id="48b5e-119">-Rule</span></span>
<span data-ttu-id="48b5e-120">Список сетевых правил</span><span class="sxs-lookup"><span data-stu-id="48b5e-120">The list of network rules</span></span>

```yaml
Type: PSAzureFirewallPolicyNetworkRule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b5e-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="48b5e-121">-TranslatedAddress</span></span>
<span data-ttu-id="48b5e-122">Преобразованный адрес для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="48b5e-122">The translated address for this NAT rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b5e-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="48b5e-123">-TranslatedPort</span></span>
<span data-ttu-id="48b5e-124">Переводной порт для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="48b5e-124">The translated port for this NAT rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b5e-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48b5e-125">-Confirm</span></span>
<span data-ttu-id="48b5e-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48b5e-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b5e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48b5e-127">-WhatIf</span></span>
<span data-ttu-id="48b5e-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48b5e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48b5e-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48b5e-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b5e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b5e-130">CommonParameters</span></span>
<span data-ttu-id="48b5e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48b5e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b5e-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48b5e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b5e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48b5e-133">INPUTS</span></span>

### <span data-ttu-id="48b5e-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="48b5e-134">None</span></span>

## <span data-ttu-id="48b5e-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48b5e-135">OUTPUTS</span></span>

### <span data-ttu-id="48b5e-136">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="48b5e-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="48b5e-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="48b5e-137">NOTES</span></span>

## <span data-ttu-id="48b5e-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48b5e-138">RELATED LINKS</span></span>
