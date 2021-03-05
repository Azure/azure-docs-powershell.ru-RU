---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9f82f3ac02e9acaf7e715ffb1eeb8c15fa4af3b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012152"
---
# <span data-ttu-id="cd1ba-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cd1ba-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="cd1ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd1ba-102">SYNOPSIS</span></span>
<span data-ttu-id="cd1ba-103">Удаляет NetworkRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="cd1ba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cd1ba-104">SYNTAX</span></span>

### <span data-ttu-id="cd1ba-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd1ba-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd1ba-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cd1ba-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd1ba-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd1ba-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd1ba-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd1ba-108">DESCRIPTION</span></span>
<span data-ttu-id="cd1ba-109">Удаляет NetworkRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="cd1ba-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cd1ba-110">EXAMPLES</span></span>

### <span data-ttu-id="cd1ba-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cd1ba-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="cd1ba-112">Name : defaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="cd1ba-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="cd1ba-113">Удаляет NetworkRuleSet для данного пространства имен Eventhub-Namespace1-1375.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="cd1ba-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cd1ba-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="cd1ba-115">Удаление NetworkRuleSet с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="cd1ba-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="cd1ba-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="cd1ba-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="cd1ba-117">Name : defaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="cd1ba-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="cd1ba-118">Удаляет NetworkRuleSet с помощью ResourceId пространства имен.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="cd1ba-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd1ba-119">PARAMETERS</span></span>

### <span data-ttu-id="cd1ba-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd1ba-120">-AsJob</span></span>
<span data-ttu-id="cd1ba-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cd1ba-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd1ba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd1ba-122">-DefaultProfile</span></span>
<span data-ttu-id="cd1ba-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd1ba-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd1ba-124">-InputObject</span></span>
<span data-ttu-id="cd1ba-125">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="cd1ba-125">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd1ba-126">-Name</span><span class="sxs-lookup"><span data-stu-id="cd1ba-126">-Name</span></span>
<span data-ttu-id="cd1ba-127">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="cd1ba-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd1ba-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd1ba-128">-PassThru</span></span>
<span data-ttu-id="cd1ba-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cd1ba-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cd1ba-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd1ba-130">-ResourceGroupName</span></span>
<span data-ttu-id="cd1ba-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cd1ba-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd1ba-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd1ba-132">-ResourceId</span></span>
<span data-ttu-id="cd1ba-133">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="cd1ba-133">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd1ba-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd1ba-134">-Confirm</span></span>
<span data-ttu-id="cd1ba-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd1ba-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd1ba-136">-WhatIf</span></span>
<span data-ttu-id="cd1ba-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd1ba-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd1ba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd1ba-139">CommonParameters</span></span>
<span data-ttu-id="cd1ba-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd1ba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="cd1ba-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd1ba-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd1ba-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cd1ba-142">INPUTS</span></span>

### <span data-ttu-id="cd1ba-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="cd1ba-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="cd1ba-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cd1ba-144">System.String</span></span>

## <span data-ttu-id="cd1ba-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cd1ba-145">OUTPUTS</span></span>

### <span data-ttu-id="cd1ba-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cd1ba-146">System.Boolean</span></span>

## <span data-ttu-id="cd1ba-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cd1ba-147">NOTES</span></span>

## <span data-ttu-id="cd1ba-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd1ba-148">RELATED LINKS</span></span>