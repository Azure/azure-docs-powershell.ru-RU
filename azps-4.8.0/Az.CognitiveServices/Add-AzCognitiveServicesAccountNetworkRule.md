---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080044"
---
# <span data-ttu-id="3f17c-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3f17c-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="3f17c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f17c-102">SYNOPSIS</span></span>
<span data-ttu-id="3f17c-103">Добавьте IpRules или VirtualNetworkRules в свойство NetworkRule учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="3f17c-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="3f17c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f17c-104">SYNTAX</span></span>

### <span data-ttu-id="3f17c-105">NetWorkRuleString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f17c-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f17c-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="3f17c-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f17c-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="3f17c-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f17c-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="3f17c-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f17c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f17c-109">DESCRIPTION</span></span>
<span data-ttu-id="3f17c-110">Командлет **Add-AzCognitiveServicesAccountNetworkRule** добавляет IpRules или VirtualNetworkRules в свойство NetworkRule учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="3f17c-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="3f17c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f17c-111">EXAMPLES</span></span>

### <span data-ttu-id="3f17c-112">Пример 1: Добавление нескольких IpRules с помощью IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3f17c-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="3f17c-113">Эта команда добавляет несколько IpRules с IpAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="3f17c-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="3f17c-114">Пример 2: Добавление VirtualNetworkRule с VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="3f17c-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="3f17c-115">Эта команда добавляет VirtualNetworkRule с VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="3f17c-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="3f17c-116">Пример 3: Добавление VirtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи</span><span class="sxs-lookup"><span data-stu-id="3f17c-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="3f17c-117">Эта команда добавляет VirtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3f17c-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="3f17c-118">Пример 4: Добавление нескольких IpRule с помощью объектов IpRule, ввод с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="3f17c-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="3f17c-119">Эта команда добавляет несколько IpRule с объектами IpRule, введенными с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="3f17c-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="3f17c-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f17c-120">PARAMETERS</span></span>

### <span data-ttu-id="3f17c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f17c-121">-DefaultProfile</span></span>
<span data-ttu-id="3f17c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f17c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f17c-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3f17c-123">-IpAddressOrRange</span></span>
<span data-ttu-id="3f17c-124">Учетная запись службы NetworkRule IpRules IpAddressOrRange в String.</span><span class="sxs-lookup"><span data-stu-id="3f17c-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="3f17c-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="3f17c-125">-IpRule</span></span>
<span data-ttu-id="3f17c-126">Учетная запись службы NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="3f17c-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="3f17c-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f17c-127">-Name</span></span>
<span data-ttu-id="3f17c-128">Имя учетной записи для самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="3f17c-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="3f17c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f17c-129">-ResourceGroupName</span></span>
<span data-ttu-id="3f17c-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f17c-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="3f17c-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3f17c-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="3f17c-132">Учетная запись службы NetworkRule VirtualNetworkRules VirtualNetworkResourceId в String.</span><span class="sxs-lookup"><span data-stu-id="3f17c-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="3f17c-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3f17c-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="3f17c-134">Учетная запись службы NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="3f17c-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="3f17c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f17c-135">-Confirm</span></span>
<span data-ttu-id="3f17c-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3f17c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f17c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f17c-137">-WhatIf</span></span>
<span data-ttu-id="3f17c-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3f17c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f17c-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3f17c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f17c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f17c-140">CommonParameters</span></span>
<span data-ttu-id="3f17c-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f17c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f17c-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f17c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f17c-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f17c-143">INPUTS</span></span>

### <span data-ttu-id="3f17c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="3f17c-144">System.String</span></span>

### <span data-ttu-id="3f17c-145">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="3f17c-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="3f17c-146">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="3f17c-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="3f17c-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f17c-147">OUTPUTS</span></span>

### <span data-ttu-id="3f17c-148">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3f17c-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="3f17c-149">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="3f17c-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="3f17c-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f17c-150">NOTES</span></span>

## <span data-ttu-id="3f17c-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f17c-151">RELATED LINKS</span></span>
