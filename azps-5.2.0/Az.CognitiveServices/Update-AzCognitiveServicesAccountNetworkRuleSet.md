---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 0f094ba8bdfa8dbf40f2af8495ee2f8cfa6fca16
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326818"
---
# <span data-ttu-id="6b426-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b426-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="6b426-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b426-102">SYNOPSIS</span></span>
<span data-ttu-id="6b426-103">Обновление свойства NetworkRule учетной записи "Когнитивные услуги"</span><span class="sxs-lookup"><span data-stu-id="6b426-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="6b426-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6b426-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b426-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b426-105">DESCRIPTION</span></span>
<span data-ttu-id="6b426-106">Командлет **Update-AzCognitiveServicesAccountNetworkRuleSet** обновляет свойство NetworkRule учетной записи Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="6b426-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="6b426-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6b426-107">EXAMPLES</span></span>

### <span data-ttu-id="6b426-108">Пример 1. Обновление всех свойств NetworkRule и правила ввода с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="6b426-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="6b426-109">Эта команда обновляет все свойства NetworkRule и правила ввода с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="6b426-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="6b426-110">Пример 2. Свойство NetworkRule "Обход обновления"</span><span class="sxs-lookup"><span data-stu-id="6b426-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="6b426-111">Это свойство "Обход команд" NetworkRule (другие свойства не изменяются).</span><span class="sxs-lookup"><span data-stu-id="6b426-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="6b426-112">Пример 3. Очистка правил NetworkRule для учетной записи службы когнитивных функций</span><span class="sxs-lookup"><span data-stu-id="6b426-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="6b426-113">Эта команда очищает правила NetworkRule учетной записи Службы восприятия (другие свойства не изменяются).</span><span class="sxs-lookup"><span data-stu-id="6b426-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="6b426-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b426-114">PARAMETERS</span></span>

### <span data-ttu-id="6b426-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="6b426-115">-DefaultAction</span></span>
<span data-ttu-id="6b426-116">Учетная запись учетной записи NetworkRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="6b426-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="6b426-117">Значение по `Deny` умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6b426-117">Default value `Deny`.</span></span>

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

### <span data-ttu-id="6b426-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b426-118">-DefaultProfile</span></span>
<span data-ttu-id="6b426-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b426-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b426-120">-IpRule</span><span class="sxs-lookup"><span data-stu-id="6b426-120">-IpRule</span></span>
<span data-ttu-id="6b426-121">Cognitive Services Account NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="6b426-121">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="6b426-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6b426-122">-Name</span></span>
<span data-ttu-id="6b426-123">Имя учетной записи службы восприятия.</span><span class="sxs-lookup"><span data-stu-id="6b426-123">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="6b426-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b426-124">-ResourceGroupName</span></span>
<span data-ttu-id="6b426-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b426-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="6b426-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6b426-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="6b426-127">Учетная запись службы NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="6b426-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="6b426-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b426-128">-Confirm</span></span>
<span data-ttu-id="6b426-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6b426-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b426-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b426-130">-WhatIf</span></span>
<span data-ttu-id="6b426-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b426-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b426-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6b426-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b426-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b426-133">CommonParameters</span></span>
<span data-ttu-id="6b426-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b426-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b426-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b426-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b426-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b426-136">INPUTS</span></span>

### <span data-ttu-id="6b426-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6b426-137">System.String</span></span>

### <span data-ttu-id="6b426-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="6b426-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="6b426-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="6b426-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="6b426-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6b426-140">OUTPUTS</span></span>

### <span data-ttu-id="6b426-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="6b426-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="6b426-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6b426-142">NOTES</span></span>

## <span data-ttu-id="6b426-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b426-143">RELATED LINKS</span></span>
