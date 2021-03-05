---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 0104c64bf65acc945609f4e2e0ae78ff288b142d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976179"
---
# <span data-ttu-id="42caf-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="42caf-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="42caf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42caf-102">SYNOPSIS</span></span>
 <span data-ttu-id="42caf-103">Добавление IpRules или VirtualNetworkRules в свойство NetworkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="42caf-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="42caf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="42caf-104">SYNTAX</span></span>

### <span data-ttu-id="42caf-105">NetWorkRuleString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42caf-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42caf-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="42caf-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42caf-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="42caf-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42caf-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="42caf-108">ResourceAccessRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42caf-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="42caf-109">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42caf-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="42caf-110">ResourceAccessRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42caf-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42caf-111">DESCRIPTION</span></span>
<span data-ttu-id="42caf-112">Командлет **Add-AzStorageAccountNetworkRule** добавляет IpRules или VirtualNetworkRules к свойству NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="42caf-112">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="42caf-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="42caf-113">EXAMPLES</span></span>

### <span data-ttu-id="42caf-114">Пример 1. Добавление нескольких IpRules с IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="42caf-114">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="42caf-115">Эта команда добавляет несколько ipRules с IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="42caf-115">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="42caf-116">Пример 2. Добавление значения VirtualNetworkRule с помощью VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="42caf-116">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="42caf-117">Эта команда добавляет virtualNetworkRule с VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="42caf-117">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="42caf-118">Пример 3. Добавление virtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи</span><span class="sxs-lookup"><span data-stu-id="42caf-118">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="42caf-119">Эта команда добавляет virtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="42caf-119">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="42caf-120">Пример 4. Добавление нескольких объектов IpRule с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="42caf-120">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="42caf-121">Эта команда добавляет несколько объектов IpRule, вводимых с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="42caf-121">This command add several IpRule with IpRule objects, input with JSON.</span></span>

### <span data-ttu-id="42caf-122">Пример 5. Добавление правила доступа к ресурсам</span><span class="sxs-lookup"><span data-stu-id="42caf-122">Example 5: Add a resource access rule</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="42caf-123">Эта команда добавляет правило доступа к ресурсам с TenantId и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="42caf-123">This command adds a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="42caf-124">Пример 6. Добавление всех правил доступа к ресурсам из одной учетной записи хранения в другую</span><span class="sxs-lookup"><span data-stu-id="42caf-124">Example 6: Add all resource access rules of one storage account to another storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1").ResourceAccessRules | Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2"
```

<span data-ttu-id="42caf-125">Эта команда получает все правила доступа к ресурсам из одной учетной записи хранения и добавляет их в другую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="42caf-125">This command gets all resource access rules from one storage account, and adds them to another storage account.</span></span>

## <span data-ttu-id="42caf-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42caf-126">PARAMETERS</span></span>

### <span data-ttu-id="42caf-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42caf-127">-AsJob</span></span>
<span data-ttu-id="42caf-128">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="42caf-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42caf-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42caf-129">-DefaultProfile</span></span>
<span data-ttu-id="42caf-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42caf-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42caf-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="42caf-131">-IPAddressOrRange</span></span>
<span data-ttu-id="42caf-132">Массив IpAddressOrRange, добавьте IpRules со входным значением IpAddressOrRange и действием по умолчанию Allow to NetworkRule Property.</span><span class="sxs-lookup"><span data-stu-id="42caf-132">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="42caf-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="42caf-133">-IPRule</span></span>
<span data-ttu-id="42caf-134">Массив объектов IpRule, добавляемого в свойство NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="42caf-134">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="42caf-135">-Name</span><span class="sxs-lookup"><span data-stu-id="42caf-135">-Name</span></span>
<span data-ttu-id="42caf-136">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="42caf-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="42caf-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="42caf-137">-ResourceAccessRule</span></span>
<span data-ttu-id="42caf-138">NetworkRule ResourceAccessRules учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="42caf-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: ResourceAccessRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42caf-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42caf-139">-ResourceGroupName</span></span>
<span data-ttu-id="42caf-140">Имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="42caf-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="42caf-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42caf-141">-ResourceId</span></span>
<span data-ttu-id="42caf-142">Строка ресурса ResourceAccessRule ResourceId учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="42caf-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42caf-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="42caf-143">-TenantId</span></span>
<span data-ttu-id="42caf-144">Строка " ResourceAccessRule TenantId" учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="42caf-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42caf-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="42caf-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="42caf-146">Массив VirtualNetworkResourceId добавит VirtualNetworkRule со входными данными VirtualNetworkResourceId и действием по умолчанию Allow to NetworkRule Property.</span><span class="sxs-lookup"><span data-stu-id="42caf-146">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="42caf-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="42caf-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="42caf-148">Массив объектов VirtualNetworkRule, которые нужно добавить в свойство NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="42caf-148">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="42caf-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42caf-149">-Confirm</span></span>
<span data-ttu-id="42caf-150">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="42caf-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42caf-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42caf-151">-WhatIf</span></span>
<span data-ttu-id="42caf-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42caf-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42caf-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="42caf-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42caf-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42caf-154">CommonParameters</span></span>
<span data-ttu-id="42caf-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42caf-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42caf-156">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42caf-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42caf-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42caf-157">INPUTS</span></span>

### <span data-ttu-id="42caf-158">System.String</span><span class="sxs-lookup"><span data-stu-id="42caf-158">System.String</span></span>

### <span data-ttu-id="42caf-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="42caf-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="42caf-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="42caf-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="42caf-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="42caf-161">OUTPUTS</span></span>

### <span data-ttu-id="42caf-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="42caf-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="42caf-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="42caf-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="42caf-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="42caf-164">NOTES</span></span>

## <span data-ttu-id="42caf-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42caf-165">RELATED LINKS</span></span>
