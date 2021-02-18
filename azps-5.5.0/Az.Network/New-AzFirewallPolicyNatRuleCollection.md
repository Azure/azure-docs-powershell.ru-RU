---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicynatrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyNatRuleCollection.md
ms.openlocfilehash: 010fd83d8b8e26e67e35afcc54b03ca0c1a5bd5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240789"
---
# <span data-ttu-id="2e8f6-101">New-AzFirewallPolicyNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="2e8f6-101">New-AzFirewallPolicyNatRuleCollection</span></span>

## <span data-ttu-id="2e8f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="2e8f6-103">Создание коллекции правил nat политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="2e8f6-103">Create a new Azure Firewall Policy Nat Rule Collection</span></span>

## <span data-ttu-id="2e8f6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2e8f6-104">SYNTAX</span></span>

```
New-AzFirewallPolicyNatRuleCollection -Name <String> -Priority <UInt32>
 -Rule <PSAzureFirewallPolicyNetworkRule> -ActionType <String> -TranslatedAddress <String>
 -TranslatedPort <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e8f6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e8f6-105">DESCRIPTION</span></span>
<span data-ttu-id="2e8f6-106">С **помощью cmdlet New-AzFirewallPolicyNatRuleCollection** создается коллекция правил NAT для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-106">The **New-AzFirewallPolicyNatRuleCollection** cmdlet creates a Nat rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="2e8f6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2e8f6-107">EXAMPLES</span></span>

### <span data-ttu-id="2e8f6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2e8f6-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyNatRuleCollection -Name NatRule1 -Priority 200 -Rule $netRule1 -ActionType "Dnat" -TranslatedAddress "192.168.0.1" -TranslatedPort "100"
```

<span data-ttu-id="2e8f6-109">В этом примере создается набор правил NAT с правилом сети.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-109">This example creates a nat rule collection with a network rule</span></span>

## <span data-ttu-id="2e8f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e8f6-110">PARAMETERS</span></span>

### <span data-ttu-id="2e8f6-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="2e8f6-111">-ActionType</span></span>
<span data-ttu-id="2e8f6-112">Тип действия правила</span><span class="sxs-lookup"><span data-stu-id="2e8f6-112">The type of the rule action</span></span>

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

### <span data-ttu-id="2e8f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e8f6-113">-DefaultProfile</span></span>
<span data-ttu-id="2e8f6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e8f6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2e8f6-115">-Name</span></span>
<span data-ttu-id="2e8f6-116">Имя коллекции сетевых правил</span><span class="sxs-lookup"><span data-stu-id="2e8f6-116">The name of the Network Rule Collection</span></span>

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

### <span data-ttu-id="2e8f6-117">-Priority</span><span class="sxs-lookup"><span data-stu-id="2e8f6-117">-Priority</span></span>
<span data-ttu-id="2e8f6-118">Приоритет коллекции правил</span><span class="sxs-lookup"><span data-stu-id="2e8f6-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="2e8f6-119">-Правило</span><span class="sxs-lookup"><span data-stu-id="2e8f6-119">-Rule</span></span>
<span data-ttu-id="2e8f6-120">Список правил сети</span><span class="sxs-lookup"><span data-stu-id="2e8f6-120">The list of network rules</span></span>

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

### <span data-ttu-id="2e8f6-121">-TranslatedAddress</span><span class="sxs-lookup"><span data-stu-id="2e8f6-121">-TranslatedAddress</span></span>
<span data-ttu-id="2e8f6-122">Переведенный адрес для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="2e8f6-122">The translated address for this NAT rule</span></span>

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

### <span data-ttu-id="2e8f6-123">-TranslatedPort</span><span class="sxs-lookup"><span data-stu-id="2e8f6-123">-TranslatedPort</span></span>
<span data-ttu-id="2e8f6-124">Переведенный порт для этого правила NAT</span><span class="sxs-lookup"><span data-stu-id="2e8f6-124">The translated port for this NAT rule</span></span>

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

### <span data-ttu-id="2e8f6-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e8f6-125">-Confirm</span></span>
<span data-ttu-id="2e8f6-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e8f6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e8f6-127">-WhatIf</span></span>
<span data-ttu-id="2e8f6-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e8f6-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e8f6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e8f6-130">CommonParameters</span></span>
<span data-ttu-id="2e8f6-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e8f6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e8f6-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2e8f6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e8f6-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2e8f6-133">INPUTS</span></span>

### <span data-ttu-id="2e8f6-134">Нет</span><span class="sxs-lookup"><span data-stu-id="2e8f6-134">None</span></span>

## <span data-ttu-id="2e8f6-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2e8f6-135">OUTPUTS</span></span>

### <span data-ttu-id="2e8f6-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="2e8f6-136">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallNetworkRuleCollection</span></span>

## <span data-ttu-id="2e8f6-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2e8f6-137">NOTES</span></span>

## <span data-ttu-id="2e8f6-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e8f6-138">RELATED LINKS</span></span>
