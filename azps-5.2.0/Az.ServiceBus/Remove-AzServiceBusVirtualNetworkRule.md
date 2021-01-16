---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusVirtualNetworkRule.md
ms.openlocfilehash: d72c7e1ebfdd7543740ea8fafeb62861f4394093
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401596"
---
# <span data-ttu-id="239db-101">Remove-AzServiceBusVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="239db-101">Remove-AzServiceBusVirtualNetworkRule</span></span>

## <span data-ttu-id="239db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="239db-102">SYNOPSIS</span></span>
<span data-ttu-id="239db-103">Удаляет отдельное заданное для NetworkRuleSet для пространства имен VirtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="239db-103">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="239db-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="239db-104">SYNTAX</span></span>

### <span data-ttu-id="239db-105">VirtualNetworkRulePropertiesParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="239db-105">VirtualNetworkRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String> [-SubnetId] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="239db-106">VirtualNetworkRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="239db-106">VirtualNetworkRuleInputObjectParameterSet</span></span>
```
Remove-AzServiceBusVirtualNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 [-VirtualNetworkRuleObject] <PSNWRuleSetVirtualNetworkRulesAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="239db-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="239db-107">DESCRIPTION</span></span>
<span data-ttu-id="239db-108">Удаляет одно заданное для NetworkRuleSet из пространства имен virtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="239db-108">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

## <span data-ttu-id="239db-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="239db-109">EXAMPLES</span></span>

### <span data-ttu-id="239db-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="239db-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -SubnetId "/subscriptions/SubscriptionId/resourcegroups/ResourceGroup/v-ajnavtest/providers/Microsoft.Network/virtualNetworks/sbehvnettest1/subnets/sbdefault01"
```

<span data-ttu-id="239db-111">Удаляет одно заданное для NetworkRuleSet из пространства имен virtualNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="239db-111">Removes the single given VirtualNetworkRule for the NetworkRuleSet of the Namespace</span></span>

### <span data-ttu-id="239db-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="239db-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzServiceBusVirtualNetworkRule -ResourceGroupName v-ajnavtest -Namespace ServiceBus-Namespace1-2389 -VirtualNetworkRuleObject $virtualruleset1
```

<span data-ttu-id="239db-113">Удаление $virtualruleset 1 NetworkRuleSet для заданного пространства имен</span><span class="sxs-lookup"><span data-stu-id="239db-113">Remove the $virtualruleset1 of NetworkRuleSet for the given Namespace</span></span>


## <span data-ttu-id="239db-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="239db-114">PARAMETERS</span></span>

### <span data-ttu-id="239db-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="239db-115">-AsJob</span></span>
<span data-ttu-id="239db-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="239db-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="239db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="239db-117">-DefaultProfile</span></span>
<span data-ttu-id="239db-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="239db-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="239db-119">-Name</span><span class="sxs-lookup"><span data-stu-id="239db-119">-Name</span></span>
<span data-ttu-id="239db-120">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="239db-120">Namespace Name</span></span>

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

### <span data-ttu-id="239db-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="239db-121">-PassThru</span></span>
<span data-ttu-id="239db-122">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="239db-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="239db-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="239db-123">-ResourceGroupName</span></span>
<span data-ttu-id="239db-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="239db-124">Resource Group Name</span></span>

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

### <span data-ttu-id="239db-125">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="239db-125">-SubnetId</span></span>
<span data-ttu-id="239db-126">ИД ресурсов подсети</span><span class="sxs-lookup"><span data-stu-id="239db-126">Subnet Resource ID</span></span>

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

### <span data-ttu-id="239db-127">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="239db-127">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="239db-128">Объект конфигурации IPRule</span><span class="sxs-lookup"><span data-stu-id="239db-128">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes
Parameter Sets: VirtualNetworkRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="239db-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="239db-129">-Confirm</span></span>
<span data-ttu-id="239db-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="239db-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="239db-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="239db-131">-WhatIf</span></span>
<span data-ttu-id="239db-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="239db-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="239db-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="239db-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="239db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="239db-134">CommonParameters</span></span>
<span data-ttu-id="239db-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="239db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="239db-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="239db-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="239db-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="239db-137">INPUTS</span></span>

### <span data-ttu-id="239db-138">System.String</span><span class="sxs-lookup"><span data-stu-id="239db-138">System.String</span></span>

### <span data-ttu-id="239db-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="239db-139">Microsoft.Azure.Commands.ServiceBus.Models.PSNWRuleSetVirtualNetworkRulesAttributes</span></span>

## <span data-ttu-id="239db-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="239db-140">OUTPUTS</span></span>

### <span data-ttu-id="239db-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="239db-141">Microsoft.Azure.Commands.ServiceBus.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="239db-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="239db-142">NOTES</span></span>

## <span data-ttu-id="239db-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="239db-143">RELATED LINKS</span></span>
