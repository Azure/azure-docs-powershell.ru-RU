---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 2faf890cda0c87d15704a14f9c4ae12c5b3d81c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326847"
---
# <span data-ttu-id="e7ab7-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e7ab7-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="e7ab7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ab7-103">Удаление IpRules или VirtualNetworkRules из свойства NetWorkRule учетной записи Службы восприятия</span><span class="sxs-lookup"><span data-stu-id="e7ab7-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="e7ab7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e7ab7-104">SYNTAX</span></span>

### <span data-ttu-id="e7ab7-105">NetWorkRuleString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e7ab7-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ab7-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="e7ab7-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7ab7-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="e7ab7-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e7ab7-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="e7ab7-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7ab7-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7ab7-109">DESCRIPTION</span></span>
<span data-ttu-id="e7ab7-110">Командлет **Remove-AzCognitiveServicesAccountNetworkRule** удаляет IpRules или VirtualNetworkRules из свойства NetWorkRule учетной записи Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="e7ab7-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e7ab7-111">EXAMPLES</span></span>

### <span data-ttu-id="e7ab7-112">Пример 1. Удаление нескольких IpRules с помощью IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e7ab7-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="e7ab7-113">Эта команда удаляет несколько ipRules с IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="e7ab7-114">Пример 2. Удаление объекта VirtualNetworkRule с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="e7ab7-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="e7ab7-115">Эта команда удаляет объект VirtualNetworkRule с объектом VirtualNetworkRule, входным с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="e7ab7-116">Пример 3. Удаление первого IpRule с конвейером</span><span class="sxs-lookup"><span data-stu-id="e7ab7-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="e7ab7-117">Эта команда удаляет первое ipRule с конвейером.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="e7ab7-118">Пример 4. Удаление нескольких virtualNetworkRules с помощью VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="e7ab7-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="e7ab7-119">Эта команда удаляет несколько виртуальныхNetworkRules с virtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="e7ab7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7ab7-120">PARAMETERS</span></span>

### <span data-ttu-id="e7ab7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ab7-121">-DefaultProfile</span></span>
<span data-ttu-id="e7ab7-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7ab7-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="e7ab7-123">-IpAddressOrRange</span></span>
<span data-ttu-id="e7ab7-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange в строке.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ab7-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="e7ab7-125">-IpRule</span></span>
<span data-ttu-id="e7ab7-126">Cognitive Services Account NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-126">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ab7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e7ab7-127">-Name</span></span>
<span data-ttu-id="e7ab7-128">Имя учетной записи службы восприятия.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="e7ab7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7ab7-129">-ResourceGroupName</span></span>
<span data-ttu-id="e7ab7-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="e7ab7-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="e7ab7-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="e7ab7-132">Учетная запись Учетной записи NetworkRule VirtualNetworkRules VirtualNetworkResourceId в строке.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7ab7-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e7ab7-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="e7ab7-134">Учетная запись Учетной записи NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ab7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7ab7-135">-Confirm</span></span>
<span data-ttu-id="e7ab7-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7ab7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7ab7-137">-WhatIf</span></span>
<span data-ttu-id="e7ab7-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7ab7-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7ab7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ab7-140">CommonParameters</span></span>
<span data-ttu-id="e7ab7-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7ab7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ab7-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7ab7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ab7-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e7ab7-143">INPUTS</span></span>

### <span data-ttu-id="e7ab7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e7ab7-144">System.String</span></span>

### <span data-ttu-id="e7ab7-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="e7ab7-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="e7ab7-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="e7ab7-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="e7ab7-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e7ab7-147">OUTPUTS</span></span>

### <span data-ttu-id="e7ab7-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e7ab7-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="e7ab7-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="e7ab7-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="e7ab7-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e7ab7-150">NOTES</span></span>

## <span data-ttu-id="e7ab7-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7ab7-151">RELATED LINKS</span></span>