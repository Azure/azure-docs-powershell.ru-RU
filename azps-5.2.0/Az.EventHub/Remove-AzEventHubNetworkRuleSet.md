---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329255"
---
# <span data-ttu-id="3f637-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3f637-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="3f637-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f637-102">SYNOPSIS</span></span>
<span data-ttu-id="3f637-103">Удаляет NetworkRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3f637-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="3f637-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f637-104">SYNTAX</span></span>

### <span data-ttu-id="3f637-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f637-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f637-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3f637-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f637-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f637-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f637-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f637-108">DESCRIPTION</span></span>
<span data-ttu-id="3f637-109">Удаляет NetworkRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3f637-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="3f637-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f637-110">EXAMPLES</span></span>

### <span data-ttu-id="3f637-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3f637-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="3f637-112">Name : defaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="3f637-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="3f637-113">Удаляет NetworkRuleSet для данного пространства имен Eventhub-Namespace1-1375.</span><span class="sxs-lookup"><span data-stu-id="3f637-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="3f637-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3f637-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="3f637-115">Удаление NetworkRuleSet с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="3f637-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="3f637-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3f637-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="3f637-117">Name : defaultAction : Allow Id : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules : VirtualNetworkRules :</span><span class="sxs-lookup"><span data-stu-id="3f637-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="3f637-118">Удаление NetworkRuleSet с помощью ResourceId пространства имен</span><span class="sxs-lookup"><span data-stu-id="3f637-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="3f637-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f637-119">PARAMETERS</span></span>

### <span data-ttu-id="3f637-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f637-120">-AsJob</span></span>
<span data-ttu-id="3f637-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3f637-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f637-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f637-122">-DefaultProfile</span></span>
<span data-ttu-id="3f637-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f637-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f637-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f637-124">-InputObject</span></span>
<span data-ttu-id="3f637-125">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="3f637-125">Namespace Object</span></span>

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

### <span data-ttu-id="3f637-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3f637-126">-Name</span></span>
<span data-ttu-id="3f637-127">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="3f637-127">Namespace Name</span></span>

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

### <span data-ttu-id="3f637-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f637-128">-PassThru</span></span>
<span data-ttu-id="3f637-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3f637-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3f637-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f637-130">-ResourceGroupName</span></span>
<span data-ttu-id="3f637-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3f637-131">Resource Group Name</span></span>

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

### <span data-ttu-id="3f637-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f637-132">-ResourceId</span></span>
<span data-ttu-id="3f637-133">Namespace Resource Id</span><span class="sxs-lookup"><span data-stu-id="3f637-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="3f637-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f637-134">-Confirm</span></span>
<span data-ttu-id="3f637-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3f637-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f637-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f637-136">-WhatIf</span></span>
<span data-ttu-id="3f637-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f637-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f637-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3f637-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f637-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f637-139">CommonParameters</span></span>
<span data-ttu-id="3f637-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f637-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3f637-141">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f637-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f637-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f637-142">INPUTS</span></span>

### <span data-ttu-id="3f637-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3f637-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="3f637-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3f637-144">System.String</span></span>

## <span data-ttu-id="3f637-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f637-145">OUTPUTS</span></span>

### <span data-ttu-id="3f637-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f637-146">System.Boolean</span></span>

## <span data-ttu-id="3f637-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f637-147">NOTES</span></span>

## <span data-ttu-id="3f637-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f637-148">RELATED LINKS</span></span>