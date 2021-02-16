---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211873"
---
# <span data-ttu-id="a5b80-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a5b80-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="a5b80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5b80-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b80-103">Добавление IpRules или VirtualNetworkRules в свойство NetworkRule учетной записи Службы восприятия</span><span class="sxs-lookup"><span data-stu-id="a5b80-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="a5b80-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a5b80-104">SYNTAX</span></span>

### <span data-ttu-id="a5b80-105">NetWorkRuleString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5b80-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5b80-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="a5b80-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b80-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="a5b80-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5b80-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="a5b80-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5b80-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5b80-109">DESCRIPTION</span></span>
<span data-ttu-id="a5b80-110">Командлет **Add-AzCognitiveServicesAccountNetworkRule** добавляет IpRules или VirtualNetworkRules к свойству NetworkRule учетной записи Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="a5b80-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="a5b80-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a5b80-111">EXAMPLES</span></span>

### <span data-ttu-id="a5b80-112">Пример 1. Добавление нескольких IpRules с ipAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="a5b80-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="a5b80-113">Эта команда добавляет несколько ipRules с IpAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="a5b80-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="a5b80-114">Пример 2. Добавление значения VirtualNetworkRule с помощью VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="a5b80-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="a5b80-115">Эта команда добавляет virtualNetworkRule с VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="a5b80-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="a5b80-116">Пример 3. Добавление virtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи</span><span class="sxs-lookup"><span data-stu-id="a5b80-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="a5b80-117">Эта команда добавляет virtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a5b80-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="a5b80-118">Пример 4. Добавление нескольких объектов IpRule с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="a5b80-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="a5b80-119">Эта команда добавляет несколько объектов IpRule, вводимых с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="a5b80-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="a5b80-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5b80-120">PARAMETERS</span></span>

### <span data-ttu-id="a5b80-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b80-121">-DefaultProfile</span></span>
<span data-ttu-id="a5b80-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b80-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b80-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="a5b80-123">-IpAddressOrRange</span></span>
<span data-ttu-id="a5b80-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange в строке.</span><span class="sxs-lookup"><span data-stu-id="a5b80-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="a5b80-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="a5b80-125">-IpRule</span></span>
<span data-ttu-id="a5b80-126">Cognitive Services Account NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="a5b80-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="a5b80-127">-Name</span><span class="sxs-lookup"><span data-stu-id="a5b80-127">-Name</span></span>
<span data-ttu-id="a5b80-128">Имя учетной записи службы восприятия.</span><span class="sxs-lookup"><span data-stu-id="a5b80-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="a5b80-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b80-129">-ResourceGroupName</span></span>
<span data-ttu-id="a5b80-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a5b80-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="a5b80-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="a5b80-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="a5b80-132">Учетная запись Учетной записи NetworkRule VirtualNetworkRules VirtualNetworkResourceId в строке.</span><span class="sxs-lookup"><span data-stu-id="a5b80-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="a5b80-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a5b80-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="a5b80-134">Учетная запись Учетной записи NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="a5b80-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="a5b80-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5b80-135">-Confirm</span></span>
<span data-ttu-id="a5b80-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a5b80-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b80-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b80-137">-WhatIf</span></span>
<span data-ttu-id="a5b80-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5b80-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b80-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a5b80-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b80-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b80-140">CommonParameters</span></span>
<span data-ttu-id="a5b80-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b80-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b80-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5b80-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b80-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5b80-143">INPUTS</span></span>

### <span data-ttu-id="a5b80-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a5b80-144">System.String</span></span>

### <span data-ttu-id="a5b80-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="a5b80-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="a5b80-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="a5b80-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="a5b80-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5b80-147">OUTPUTS</span></span>

### <span data-ttu-id="a5b80-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a5b80-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="a5b80-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="a5b80-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="a5b80-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a5b80-150">NOTES</span></span>

## <span data-ttu-id="a5b80-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5b80-151">RELATED LINKS</span></span>
