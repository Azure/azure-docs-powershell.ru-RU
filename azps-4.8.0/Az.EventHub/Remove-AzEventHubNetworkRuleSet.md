---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 9c263e4d31d5d186abb4a08f3849db072aec3721
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244962"
---
# <span data-ttu-id="921b0-101">Remove-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="921b0-101">Remove-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="921b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="921b0-102">SYNOPSIS</span></span>
<span data-ttu-id="921b0-103">Удаляет NetworkRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="921b0-103">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="921b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="921b0-104">SYNTAX</span></span>

### <span data-ttu-id="921b0-105">NetworkRuleSetPropertiesSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="921b0-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="921b0-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="921b0-106">NamespaceInputObjectSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-InputObject] <PSNamespaceAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="921b0-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="921b0-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Remove-AzEventHubNetworkRuleSet [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="921b0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="921b0-108">DESCRIPTION</span></span>
<span data-ttu-id="921b0-109">Удаляет NetworkRuleSet для заданного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="921b0-109">Removes the NetworkRuleSet for the Given Namespace</span></span>

## <span data-ttu-id="921b0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="921b0-110">EXAMPLES</span></span>

### <span data-ttu-id="921b0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="921b0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="921b0-112">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="921b0-112">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 


<span data-ttu-id="921b0-113">Удаляет NetworkRuleSet для заданного пространства имен "Eventhub-Namespace1-1375"</span><span class="sxs-lookup"><span data-stu-id="921b0-113">Deletes the NetworkRuleSet for the Given "Eventhub-Namespace1-1375" namespace</span></span> 

### <span data-ttu-id="921b0-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="921b0-114">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -InputObject $result1375
```

<span data-ttu-id="921b0-115">Удаление NetworkRuleSet с помощью InputObject</span><span class="sxs-lookup"><span data-stu-id="921b0-115">Deletes the NetworkRuleSet using InputObject</span></span> 

### <span data-ttu-id="921b0-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="921b0-116">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-1375 -PassThru
```
<span data-ttu-id="921b0-117">Имя: по умолчанию DefaultAction: Allow ID:/subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type: Microsoft. EventHub/Namespaces/NetworkRuleSet IpRules: VirtualNetworkRules:</span><span class="sxs-lookup"><span data-stu-id="921b0-117">Name                : default DefaultAction       : Allow Id                  : /subscriptions/subscriptionId/resourceGroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/EventHub-Namespace-1375/networkRuleSets/default Type                : Microsoft.EventHub/Namespaces/NetworkRuleSet IpRules             : VirtualNetworkRules :</span></span> 

<span data-ttu-id="921b0-118">Удаляет NetworkRuleSet, использующий ResourceId из пространства имен</span><span class="sxs-lookup"><span data-stu-id="921b0-118">Deletes the NetworkRuleSet using ResourceId of the Namespace</span></span>


## <span data-ttu-id="921b0-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="921b0-119">PARAMETERS</span></span>

### <span data-ttu-id="921b0-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="921b0-120">-AsJob</span></span>
<span data-ttu-id="921b0-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="921b0-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="921b0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="921b0-122">-DefaultProfile</span></span>
<span data-ttu-id="921b0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="921b0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="921b0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="921b0-124">-InputObject</span></span>
<span data-ttu-id="921b0-125">Объект Namespace</span><span class="sxs-lookup"><span data-stu-id="921b0-125">Namespace Object</span></span>

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

### <span data-ttu-id="921b0-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="921b0-126">-Name</span></span>
<span data-ttu-id="921b0-127">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="921b0-127">Namespace Name</span></span>

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

### <span data-ttu-id="921b0-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="921b0-128">-PassThru</span></span>
<span data-ttu-id="921b0-129">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="921b0-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="921b0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="921b0-130">-ResourceGroupName</span></span>
<span data-ttu-id="921b0-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="921b0-131">Resource Group Name</span></span>

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

### <span data-ttu-id="921b0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="921b0-132">-ResourceId</span></span>
<span data-ttu-id="921b0-133">Идентификатор ресурса пространства имен</span><span class="sxs-lookup"><span data-stu-id="921b0-133">Namespace Resource Id</span></span>

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

### <span data-ttu-id="921b0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="921b0-134">-Confirm</span></span>
<span data-ttu-id="921b0-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="921b0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="921b0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="921b0-136">-WhatIf</span></span>
<span data-ttu-id="921b0-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="921b0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="921b0-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="921b0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="921b0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="921b0-139">CommonParameters</span></span>
<span data-ttu-id="921b0-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="921b0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="921b0-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="921b0-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="921b0-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="921b0-142">INPUTS</span></span>

### <span data-ttu-id="921b0-143">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="921b0-143">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="921b0-144">System. String</span><span class="sxs-lookup"><span data-stu-id="921b0-144">System.String</span></span>

## <span data-ttu-id="921b0-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="921b0-145">OUTPUTS</span></span>

### <span data-ttu-id="921b0-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="921b0-146">System.Boolean</span></span>

## <span data-ttu-id="921b0-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="921b0-147">NOTES</span></span>

## <span data-ttu-id="921b0-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="921b0-148">RELATED LINKS</span></span>