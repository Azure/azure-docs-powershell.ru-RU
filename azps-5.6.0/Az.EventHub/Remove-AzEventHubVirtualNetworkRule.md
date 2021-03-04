---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 3d8221d36cdd6ec0845f3f26dfe1526f796c2213
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990293"
---
# <span data-ttu-id="35903-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="35903-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="35903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35903-102">SYNOPSIS</span></span>
<span data-ttu-id="35903-103">Удаляет одно заданное для NetworkRuleSet из пространства имен virtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="35903-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="35903-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35903-104">SYNTAX</span></span>

### <span data-ttu-id="35903-105">VirtualNetworkRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35903-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35903-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35903-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35903-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35903-107">DESCRIPTION</span></span>
<span data-ttu-id="35903-108">Удаляет одно заданное для NetworkRuleSet из пространства имен virtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="35903-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="35903-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35903-109">EXAMPLES</span></span>

### <span data-ttu-id="35903-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35903-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="35903-111">Удаляет одно заданное для NetworkRuleSet из пространства имен virtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="35903-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="35903-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="35903-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="35903-113">Удаление $virtualruleset 1 NetworkRuleSet для заданного пространства имен</span><span class="sxs-lookup"><span data-stu-id="35903-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="35903-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35903-114">PARAMETERS</span></span>

### <span data-ttu-id="35903-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35903-115">-AsJob</span></span>
<span data-ttu-id="35903-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="35903-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35903-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35903-117">-DefaultProfile</span></span>
<span data-ttu-id="35903-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35903-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35903-119">-Name</span><span class="sxs-lookup"><span data-stu-id="35903-119">-Name</span></span>
<span data-ttu-id="35903-120">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="35903-120">Namespace Name</span></span>

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

### <span data-ttu-id="35903-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35903-121">-PassThru</span></span>
<span data-ttu-id="35903-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="35903-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="35903-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35903-123">-ResourceGroupName</span></span>
<span data-ttu-id="35903-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="35903-124">Resource Group Name</span></span>

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

### <span data-ttu-id="35903-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="35903-125">-SubnetId</span></span>
<span data-ttu-id="35903-126">ИД ресурсов подсети</span><span class="sxs-lookup"><span data-stu-id="35903-126">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualNetworkRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35903-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="35903-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="35903-128">Объект конфигурации IPRule</span><span class="sxs-lookup"><span data-stu-id="35903-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35903-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35903-129">-Confirm</span></span>
<span data-ttu-id="35903-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35903-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35903-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35903-131">-WhatIf</span></span>
<span data-ttu-id="35903-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35903-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35903-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="35903-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35903-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35903-134">CommonParameters</span></span>
<span data-ttu-id="35903-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35903-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="35903-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35903-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35903-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35903-137">INPUTS</span></span>

### <span data-ttu-id="35903-138">System.String</span><span class="sxs-lookup"><span data-stu-id="35903-138">System.String</span></span>

### <span data-ttu-id="35903-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="35903-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="35903-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35903-140">OUTPUTS</span></span>

### <span data-ttu-id="35903-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="35903-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="35903-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35903-142">NOTES</span></span>

## <span data-ttu-id="35903-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35903-143">RELATED LINKS</span></span>