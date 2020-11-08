---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246409"
---
# <span data-ttu-id="c51a0-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c51a0-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="c51a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c51a0-102">SYNOPSIS</span></span>
<span data-ttu-id="c51a0-103">Создание коллекции правил для новой политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="c51a0-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="c51a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c51a0-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c51a0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c51a0-105">DESCRIPTION</span></span>
<span data-ttu-id="c51a0-106">Командлет **New-AzFirewallPolicyFilterRuleCollection** создает коллекцию правил фильтрации для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="c51a0-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="c51a0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c51a0-107">EXAMPLES</span></span>

### <span data-ttu-id="c51a0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c51a0-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="c51a0-109">В этом примере создается правило фильтра с двумя условиями правил</span><span class="sxs-lookup"><span data-stu-id="c51a0-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="c51a0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c51a0-110">PARAMETERS</span></span>

### <span data-ttu-id="c51a0-111">-Себя</span><span class="sxs-lookup"><span data-stu-id="c51a0-111">-ActionType</span></span>
<span data-ttu-id="c51a0-112">Действие коллекции правил</span><span class="sxs-lookup"><span data-stu-id="c51a0-112">The action of the rule collection</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c51a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c51a0-113">-DefaultProfile</span></span>
<span data-ttu-id="c51a0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c51a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c51a0-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c51a0-115">-Name</span></span>
<span data-ttu-id="c51a0-116">Имя коллекции правил приложений</span><span class="sxs-lookup"><span data-stu-id="c51a0-116">The name of the Application Rule Collection</span></span>

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

### <span data-ttu-id="c51a0-117">-Priority (приоритет)</span><span class="sxs-lookup"><span data-stu-id="c51a0-117">-Priority</span></span>
<span data-ttu-id="c51a0-118">Приоритет коллекции правил</span><span class="sxs-lookup"><span data-stu-id="c51a0-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="c51a0-119">-Правило</span><span class="sxs-lookup"><span data-stu-id="c51a0-119">-Rule</span></span>
<span data-ttu-id="c51a0-120">Список правил приложений</span><span class="sxs-lookup"><span data-stu-id="c51a0-120">The list of application rules</span></span>

```yaml
Type: PSAzureFirewallPolicyRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c51a0-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c51a0-121">-Confirm</span></span>
<span data-ttu-id="c51a0-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c51a0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c51a0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c51a0-123">-WhatIf</span></span>
<span data-ttu-id="c51a0-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c51a0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c51a0-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c51a0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c51a0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c51a0-126">CommonParameters</span></span>
<span data-ttu-id="c51a0-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c51a0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c51a0-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c51a0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c51a0-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c51a0-129">INPUTS</span></span>

### <span data-ttu-id="c51a0-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="c51a0-130">None</span></span>

## <span data-ttu-id="c51a0-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c51a0-131">OUTPUTS</span></span>

### <span data-ttu-id="c51a0-132">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="c51a0-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="c51a0-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c51a0-133">NOTES</span></span>

## <span data-ttu-id="c51a0-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c51a0-134">RELATED LINKS</span></span>
