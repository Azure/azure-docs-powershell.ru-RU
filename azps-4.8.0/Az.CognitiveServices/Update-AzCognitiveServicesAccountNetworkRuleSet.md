---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 0f094ba8bdfa8dbf40f2af8495ee2f8cfa6fca16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236890"
---
# <span data-ttu-id="ac0b2-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac0b2-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="ac0b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ac0b2-103">Обновление свойства NetworkRule учетной записи службы для персонализированных служб</span><span class="sxs-lookup"><span data-stu-id="ac0b2-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="ac0b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac0b2-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac0b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac0b2-105">DESCRIPTION</span></span>
<span data-ttu-id="ac0b2-106">Командлет **Update-AzCognitiveServicesAccountNetworkRuleSet** обновляет свойство NetworkRule учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="ac0b2-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="ac0b2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac0b2-107">EXAMPLES</span></span>

### <span data-ttu-id="ac0b2-108">Пример 1: обновление всех свойств NetworkRule, правил ввода с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="ac0b2-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="ac0b2-109">Эта команда обновляет все свойства NetworkRule, правила ввода с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="ac0b2-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="ac0b2-110">Пример 2: обновление свойства обхода для NetworkRule</span><span class="sxs-lookup"><span data-stu-id="ac0b2-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="ac0b2-111">Это обновление свойства обхода для NetworkRule (другие свойства не изменяются).</span><span class="sxs-lookup"><span data-stu-id="ac0b2-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="ac0b2-112">Пример 3: Очистка правил NetworkRule учетной записи службы</span><span class="sxs-lookup"><span data-stu-id="ac0b2-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="ac0b2-113">Эта команда очищает правила для NetworkRule учетной записи службы (другие свойства не изменяются).</span><span class="sxs-lookup"><span data-stu-id="ac0b2-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="ac0b2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac0b2-114">PARAMETERS</span></span>

### <span data-ttu-id="ac0b2-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="ac0b2-115">-DefaultAction</span></span>
<span data-ttu-id="ac0b2-116">Учетная запись службы NetworkRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="ac0b2-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="ac0b2-117">Значение по умолчанию `Deny` .</span><span class="sxs-lookup"><span data-stu-id="ac0b2-117">Default value `Deny`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac0b2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac0b2-118">-DefaultProfile</span></span>
<span data-ttu-id="ac0b2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac0b2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac0b2-120">-IpRule</span><span class="sxs-lookup"><span data-stu-id="ac0b2-120">-IpRule</span></span>
<span data-ttu-id="ac0b2-121">Учетная запись службы NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="ac0b2-121">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac0b2-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac0b2-122">-Name</span></span>
<span data-ttu-id="ac0b2-123">Имя учетной записи для самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="ac0b2-123">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac0b2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac0b2-124">-ResourceGroupName</span></span>
<span data-ttu-id="ac0b2-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac0b2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ac0b2-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ac0b2-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="ac0b2-127">Учетная запись службы NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="ac0b2-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac0b2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac0b2-128">-Confirm</span></span>
<span data-ttu-id="ac0b2-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac0b2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac0b2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac0b2-130">-WhatIf</span></span>
<span data-ttu-id="ac0b2-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac0b2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac0b2-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac0b2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac0b2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac0b2-133">CommonParameters</span></span>
<span data-ttu-id="ac0b2-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac0b2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac0b2-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac0b2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac0b2-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac0b2-136">INPUTS</span></span>

### <span data-ttu-id="ac0b2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ac0b2-137">System.String</span></span>

### <span data-ttu-id="ac0b2-138">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="ac0b2-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="ac0b2-139">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="ac0b2-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="ac0b2-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac0b2-140">OUTPUTS</span></span>

### <span data-ttu-id="ac0b2-141">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ac0b2-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="ac0b2-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac0b2-142">NOTES</span></span>

## <span data-ttu-id="ac0b2-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac0b2-143">RELATED LINKS</span></span>
