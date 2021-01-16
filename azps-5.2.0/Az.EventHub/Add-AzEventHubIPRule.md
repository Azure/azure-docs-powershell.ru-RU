---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/add-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Add-AzEventHubIPRule.md
ms.openlocfilehash: 54846520fd8370d171a20970eda1d42af81e4d0c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412839"
---
# <span data-ttu-id="e3ec0-101">Add-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="e3ec0-101">Add-AzEventHubIPRule</span></span>

## <span data-ttu-id="e3ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ec0-103">Добавление одного правила IP-адреса в NetworkRuleSet данного пространства имен</span><span class="sxs-lookup"><span data-stu-id="e3ec0-103">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="e3ec0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e3ec0-104">SYNTAX</span></span>

### <span data-ttu-id="e3ec0-105">IPRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3ec0-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String> [-Action <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3ec0-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3ec0-106">IPRuleInputObjectParameterSet</span></span>
```
Add-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3ec0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3ec0-107">DESCRIPTION</span></span>
<span data-ttu-id="e3ec0-108">Добавление одного правила IP-адреса в NetworkRuleSet данного пространства имен</span><span class="sxs-lookup"><span data-stu-id="e3ec0-108">Add a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="e3ec0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e3ec0-109">EXAMPLES</span></span>

### <span data-ttu-id="e3ec0-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e3ec0-110">Example 1</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44" -Action Allow
```
<span data-ttu-id="e3ec0-111">Name : defaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="e3ec0-111">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="e3ec0-112">добавьте IPRule с IpMask "11.22.33.44" и action Allow for the given namespace.</span><span class="sxs-lookup"><span data-stu-id="e3ec0-112">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

### <span data-ttu-id="e3ec0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e3ec0-113">Example 2</span></span>
```powershell
PS C:\> Add-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpRuleObject $ipruleobject
```
<span data-ttu-id="e3ec0-114">Name : defaultAction : Allow Id : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules : {11.22.33.44, Allow} VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="e3ec0-114">Name                : default DefaultAction       : Allow Id                  : /subscriptions/SubscriptionId/resourceGroups/RSG-TestAzEventhub/providers/Microsoft.Eventhub/namespaces/Eventhub-Namespace-2389/networkRuleSets/default Type                : Microsoft.Eventhub/Namespaces/NetworkRuleSet IpRules             : {11.22.33.44, Allow} VirtualNetworkRules :</span></span> 

<span data-ttu-id="e3ec0-115">добавьте IPRule с IpMask "11.22.33.44" и action Allow for the given namespace.</span><span class="sxs-lookup"><span data-stu-id="e3ec0-115">add the IPRule with IpMask "11.22.33.44" and Action Allow for the given namespace.</span></span>

## <span data-ttu-id="e3ec0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3ec0-116">PARAMETERS</span></span>

### <span data-ttu-id="e3ec0-117">-Action</span><span class="sxs-lookup"><span data-stu-id="e3ec0-117">-Action</span></span>
<span data-ttu-id="e3ec0-118">Действие фильтра IP-адресов</span><span class="sxs-lookup"><span data-stu-id="e3ec0-118">The IP Filter Action</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3ec0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ec0-119">-DefaultProfile</span></span>
<span data-ttu-id="e3ec0-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3ec0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3ec0-121">-IpMask</span><span class="sxs-lookup"><span data-stu-id="e3ec0-121">-IpMask</span></span>
<span data-ttu-id="e3ec0-122">ИД ресурсов подсети</span><span class="sxs-lookup"><span data-stu-id="e3ec0-122">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3ec0-123">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="e3ec0-123">-IpRuleObject</span></span>
<span data-ttu-id="e3ec0-124">Объект конфигурации IPRule, который нужно добавить</span><span class="sxs-lookup"><span data-stu-id="e3ec0-124">IPRule Configuration Object to be added</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3ec0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e3ec0-125">-Name</span></span>
<span data-ttu-id="e3ec0-126">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="e3ec0-126">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3ec0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ec0-127">-ResourceGroupName</span></span>
<span data-ttu-id="e3ec0-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e3ec0-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3ec0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3ec0-129">-Confirm</span></span>
<span data-ttu-id="e3ec0-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3ec0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3ec0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3ec0-131">-WhatIf</span></span>
<span data-ttu-id="e3ec0-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3ec0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3ec0-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e3ec0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3ec0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ec0-134">CommonParameters</span></span>
<span data-ttu-id="e3ec0-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3ec0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e3ec0-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3ec0-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ec0-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3ec0-137">INPUTS</span></span>

### <span data-ttu-id="e3ec0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="e3ec0-138">System.String</span></span>

### <span data-ttu-id="e3ec0-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="e3ec0-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="e3ec0-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e3ec0-140">OUTPUTS</span></span>

### <span data-ttu-id="e3ec0-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="e3ec0-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="e3ec0-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e3ec0-142">NOTES</span></span>

## <span data-ttu-id="e3ec0-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3ec0-143">RELATED LINKS</span></span>
