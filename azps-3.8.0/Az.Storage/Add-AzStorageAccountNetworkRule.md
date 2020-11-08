---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073474"
---
# <span data-ttu-id="b951e-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b951e-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="b951e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b951e-102">SYNOPSIS</span></span>
 <span data-ttu-id="b951e-103">Добавление IpRules или VirtualNetworkRules в свойство NetworkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b951e-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="b951e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b951e-104">SYNTAX</span></span>

### <span data-ttu-id="b951e-105">NetWorkRuleString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b951e-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b951e-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="b951e-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b951e-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="b951e-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b951e-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="b951e-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b951e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b951e-109">DESCRIPTION</span></span>
<span data-ttu-id="b951e-110">Командлет **Add-AzStorageAccountNetworkRule** добавляет IpRules или VirtualNetworkRules в свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b951e-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="b951e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b951e-111">EXAMPLES</span></span>

### <span data-ttu-id="b951e-112">Пример 1: Добавление нескольких IpRules с помощью IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b951e-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="b951e-113">Эта команда добавляет несколько IpRules с IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="b951e-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="b951e-114">Пример 2: Добавление VirtualNetworkRule с VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="b951e-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="b951e-115">Эта команда добавляет VirtualNetworkRule с VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="b951e-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="b951e-116">Пример 3: Добавление VirtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи</span><span class="sxs-lookup"><span data-stu-id="b951e-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="b951e-117">Эта команда добавляет VirtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="b951e-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="b951e-118">Пример 4: Добавление нескольких IpRule с помощью объектов IpRule, ввод с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="b951e-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="b951e-119">Эта команда добавляет несколько IpRule с объектами IpRule, введенными с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="b951e-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="b951e-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b951e-120">PARAMETERS</span></span>

### <span data-ttu-id="b951e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b951e-121">-AsJob</span></span>
<span data-ttu-id="b951e-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b951e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b951e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b951e-123">-DefaultProfile</span></span>
<span data-ttu-id="b951e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b951e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b951e-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b951e-125">-IPAddressOrRange</span></span>
<span data-ttu-id="b951e-126">Массив IpAddressOrRange добавьте IpRules с входными IpAddressOrRange и действием по умолчанию, допускающим NetworkRule свойство.</span><span class="sxs-lookup"><span data-stu-id="b951e-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="b951e-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="b951e-127">-IPRule</span></span>
<span data-ttu-id="b951e-128">Массив объектов IpRule, которые нужно добавить в свойство NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="b951e-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b951e-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b951e-129">-Name</span></span>
<span data-ttu-id="b951e-130">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b951e-130">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b951e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b951e-131">-ResourceGroupName</span></span>
<span data-ttu-id="b951e-132">Указывает, что имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="b951e-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="b951e-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="b951e-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="b951e-134">Массив VirtualNetworkResourceId добавит VirtualNetworkRule с входными VirtualNetworkResourceId и действием по умолчанию, допускающим NetworkRule свойство.</span><span class="sxs-lookup"><span data-stu-id="b951e-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="b951e-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b951e-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="b951e-136">Массив объектов VirtualNetworkRule, которые нужно добавить в свойство NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="b951e-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b951e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b951e-137">-Confirm</span></span>
<span data-ttu-id="b951e-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b951e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b951e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b951e-139">-WhatIf</span></span>
<span data-ttu-id="b951e-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b951e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b951e-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b951e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b951e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b951e-142">CommonParameters</span></span>
<span data-ttu-id="b951e-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b951e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b951e-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b951e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b951e-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b951e-145">INPUTS</span></span>

### <span data-ttu-id="b951e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b951e-146">System.String</span></span>

### <span data-ttu-id="b951e-147">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="b951e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="b951e-148">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="b951e-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="b951e-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b951e-149">OUTPUTS</span></span>

### <span data-ttu-id="b951e-150">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b951e-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="b951e-151">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="b951e-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="b951e-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="b951e-152">NOTES</span></span>

## <span data-ttu-id="b951e-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b951e-153">RELATED LINKS</span></span>
