---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyfilterrulecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyFilterRuleCollection.md
ms.openlocfilehash: d5871a9e1a99a27cc0b2728ca3638a0548f42fc6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225932"
---
# <span data-ttu-id="91c36-101">New-AzFirewallPolicyFilterRuleCollection</span><span class="sxs-lookup"><span data-stu-id="91c36-101">New-AzFirewallPolicyFilterRuleCollection</span></span>

## <span data-ttu-id="91c36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91c36-102">SYNOPSIS</span></span>
<span data-ttu-id="91c36-103">Создание коллекции правил фильтра политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="91c36-103">Create a new Azure Firewall Policy Filter Rule Collection</span></span>

## <span data-ttu-id="91c36-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="91c36-104">SYNTAX</span></span>

```
New-AzFirewallPolicyFilterRuleCollection -Name <String> -Priority <UInt32> -Rule <PSAzureFirewallPolicyRule[]>
 -ActionType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91c36-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91c36-105">DESCRIPTION</span></span>
<span data-ttu-id="91c36-106">С **помощью cmdlet New-AzFirewallPolicyFilterRuleCollection** создается коллекция правил фильтра для политики брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="91c36-106">The **New-AzFirewallPolicyFilterRuleCollection** cmdlet creates a Filter rule collection for a Azure Firewall Policy.</span></span>

## <span data-ttu-id="91c36-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="91c36-107">EXAMPLES</span></span>

### <span data-ttu-id="91c36-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="91c36-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallPolicyFilterRuleCollection -Name FR1 -Priority 400 -Rule $appRule1 ,$appRule2 -ActionType "Allow"
```

<span data-ttu-id="91c36-109">В этом примере создается правило фильтра с 2 условиями правила</span><span class="sxs-lookup"><span data-stu-id="91c36-109">This example creates a Filter rule with 2 rule conditions</span></span>

## <span data-ttu-id="91c36-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91c36-110">PARAMETERS</span></span>

### <span data-ttu-id="91c36-111">-ActionType</span><span class="sxs-lookup"><span data-stu-id="91c36-111">-ActionType</span></span>
<span data-ttu-id="91c36-112">Действие в наборе правил</span><span class="sxs-lookup"><span data-stu-id="91c36-112">The action of the rule collection</span></span>

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

### <span data-ttu-id="91c36-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c36-113">-DefaultProfile</span></span>
<span data-ttu-id="91c36-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91c36-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91c36-115">-Name</span><span class="sxs-lookup"><span data-stu-id="91c36-115">-Name</span></span>
<span data-ttu-id="91c36-116">Имя коллекции правил приложений</span><span class="sxs-lookup"><span data-stu-id="91c36-116">The name of the Application Rule Collection</span></span>

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

### <span data-ttu-id="91c36-117">-Priority</span><span class="sxs-lookup"><span data-stu-id="91c36-117">-Priority</span></span>
<span data-ttu-id="91c36-118">Приоритет коллекции правил</span><span class="sxs-lookup"><span data-stu-id="91c36-118">The priority of the rule collection</span></span>

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

### <span data-ttu-id="91c36-119">-Правило</span><span class="sxs-lookup"><span data-stu-id="91c36-119">-Rule</span></span>
<span data-ttu-id="91c36-120">Список правил приложения</span><span class="sxs-lookup"><span data-stu-id="91c36-120">The list of application rules</span></span>

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

### <span data-ttu-id="91c36-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91c36-121">-Confirm</span></span>
<span data-ttu-id="91c36-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="91c36-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91c36-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91c36-123">-WhatIf</span></span>
<span data-ttu-id="91c36-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91c36-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91c36-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="91c36-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91c36-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c36-126">CommonParameters</span></span>
<span data-ttu-id="91c36-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c36-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c36-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91c36-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c36-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91c36-129">INPUTS</span></span>

### <span data-ttu-id="91c36-130">Нет</span><span class="sxs-lookup"><span data-stu-id="91c36-130">None</span></span>

## <span data-ttu-id="91c36-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="91c36-131">OUTPUTS</span></span>

### <span data-ttu-id="91c36-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="91c36-132">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="91c36-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="91c36-133">NOTES</span></span>

## <span data-ttu-id="91c36-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91c36-134">RELATED LINKS</span></span>
