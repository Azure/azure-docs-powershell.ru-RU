---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubVirtualNetworkRule.md
ms.openlocfilehash: 9385d8ca958eab28f485e56fbcd6c926f5422ca0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910367"
---
# <span data-ttu-id="0865b-101">Remove-AzEventHubVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0865b-101">Remove-AzEventHubVirtualNetworkRule</span></span>

## <span data-ttu-id="0865b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0865b-102">SYNOPSIS</span></span>
<span data-ttu-id="0865b-103">Удаляет один из указанных VirtualNetworkRule для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="0865b-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="0865b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0865b-104">SYNTAX</span></span>

### <span data-ttu-id="0865b-105">VirtualNetworkRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0865b-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0865b-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0865b-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0865b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0865b-107">DESCRIPTION</span></span>
<span data-ttu-id="0865b-108">Удаляет один из указанных VirtualNetworkRule для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="0865b-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="0865b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0865b-109">EXAMPLES</span></span>

### <span data-ttu-id="0865b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0865b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="0865b-111">Удаляет один из указанных VirtualNetworkRule для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="0865b-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="0865b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0865b-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="0865b-113">Удаление $virtualruleset 1 из NetworkRuleSet для указанного пространства имен</span><span class="sxs-lookup"><span data-stu-id="0865b-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="0865b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0865b-114">PARAMETERS</span></span>

### <span data-ttu-id="0865b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0865b-115">-AsJob</span></span>
<span data-ttu-id="0865b-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0865b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0865b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0865b-117">-DefaultProfile</span></span>
<span data-ttu-id="0865b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0865b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0865b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0865b-119">-Name</span></span>
<span data-ttu-id="0865b-120">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="0865b-120">Namespace Name</span></span>

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

### <span data-ttu-id="0865b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0865b-121">-PassThru</span></span>
<span data-ttu-id="0865b-122">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="0865b-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0865b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0865b-123">-ResourceGroupName</span></span>
<span data-ttu-id="0865b-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="0865b-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0865b-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0865b-125">-SubnetId</span></span>
<span data-ttu-id="0865b-126">Идентификатор ресурса подсети</span><span class="sxs-lookup"><span data-stu-id="0865b-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="0865b-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="0865b-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="0865b-128">Объект конфигурации IPRule</span><span class="sxs-lookup"><span data-stu-id="0865b-128">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="0865b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0865b-129">-Confirm</span></span>
<span data-ttu-id="0865b-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0865b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0865b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0865b-131">-WhatIf</span></span>
<span data-ttu-id="0865b-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0865b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0865b-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0865b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0865b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0865b-134">CommonParameters</span></span>
<span data-ttu-id="0865b-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0865b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0865b-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0865b-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0865b-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0865b-137">INPUTS</span></span>

### <span data-ttu-id="0865b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0865b-138">System.String</span></span>

### <span data-ttu-id="0865b-139">Microsoft. Azure. Commands. EventHub. Models. PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="0865b-139">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="0865b-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0865b-140">OUTPUTS</span></span>

### <span data-ttu-id="0865b-141">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="0865b-141">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="0865b-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="0865b-142">NOTES</span></span>

## <span data-ttu-id="0865b-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0865b-143">RELATED LINKS</span></span>