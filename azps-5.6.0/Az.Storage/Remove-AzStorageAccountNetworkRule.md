---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 295f79f48ffa966024561486745cdcf52ec8e38f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973331"
---
# <span data-ttu-id="c6a44-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c6a44-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="c6a44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6a44-102">SYNOPSIS</span></span>
<span data-ttu-id="c6a44-103">Удаление IpRules или VirtualNetworkRules из свойства NetWorkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="c6a44-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="c6a44-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c6a44-104">SYNTAX</span></span>

### <span data-ttu-id="c6a44-105">NetWorkRuleString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c6a44-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c6a44-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="c6a44-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6a44-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="c6a44-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6a44-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="c6a44-108">ResourceAccessRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6a44-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="c6a44-109">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6a44-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="c6a44-110">ResourceAccessRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6a44-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6a44-111">DESCRIPTION</span></span>
<span data-ttu-id="c6a44-112">Командлет **Remove-AzStorageAccountNetworkRule** удаляет IpRules или VirtualNetworkRules из свойства NetWorkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c6a44-112">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="c6a44-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c6a44-113">EXAMPLES</span></span>

### <span data-ttu-id="c6a44-114">Пример 1. Удаление нескольких IpRules с помощью IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c6a44-114">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="c6a44-115">Эта команда удаляет несколько ipRules с IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="c6a44-115">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="c6a44-116">Пример 2. Удаление объекта VirtualNetworkRule с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="c6a44-116">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="c6a44-117">Эта команда удаляет объект VirtualNetworkRule с объектом VirtualNetworkRule, входным с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="c6a44-117">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="c6a44-118">Пример 3. Удаление первого IpRule с конвейером</span><span class="sxs-lookup"><span data-stu-id="c6a44-118">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="c6a44-119">Эта команда удаляет первое ipRule с конвейером.</span><span class="sxs-lookup"><span data-stu-id="c6a44-119">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="c6a44-120">Пример 4. Удаление нескольких virtualNetworkRules с помощью VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="c6a44-120">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="c6a44-121">Эта команда удаляет несколько виртуальныхNetworkRules с virtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="c6a44-121">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="c6a44-122">Пример 5. Удаление правила доступа к ресурсам с tenantId и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c6a44-122">Example 5: Remove a resource access rule with TenantId and ResourceId.</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"  -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="c6a44-123">Эта команда удаляет правило доступа к ресурсам с TenantId и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c6a44-123">This command removes a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="c6a44-124">Пример 6. Удаление первых 3 правил доступа к ресурсам из учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="c6a44-124">Example 6: Remove the first 3 resource access rules from a storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount").ResourceAccessRules | Select-Object -First 3 | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="c6a44-125">Эта команда удаляет из учетной записи хранения первые 3 правила доступа к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="c6a44-125">This command removes the first 3 resource access rules from a storage account.</span></span>

## <span data-ttu-id="c6a44-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6a44-126">PARAMETERS</span></span>

### <span data-ttu-id="c6a44-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6a44-127">-AsJob</span></span>
<span data-ttu-id="c6a44-128">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c6a44-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6a44-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6a44-129">-DefaultProfile</span></span>
<span data-ttu-id="c6a44-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6a44-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6a44-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c6a44-131">-IPAddressOrRange</span></span>
<span data-ttu-id="c6a44-132">Массив IpAddressOrRange удаляет IpRule с тем же ipAddressOrRange из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="c6a44-132">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="c6a44-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="c6a44-133">-IPRule</span></span>
<span data-ttu-id="c6a44-134">Массив объектов IpRule, удаляемого из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="c6a44-134">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="c6a44-135">-Name</span><span class="sxs-lookup"><span data-stu-id="c6a44-135">-Name</span></span>
<span data-ttu-id="c6a44-136">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c6a44-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="c6a44-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="c6a44-137">-ResourceAccessRule</span></span>
<span data-ttu-id="c6a44-138">NetworkRule ResourceAccessRules для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c6a44-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

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

### <span data-ttu-id="c6a44-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6a44-139">-ResourceGroupName</span></span>
<span data-ttu-id="c6a44-140">Имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="c6a44-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="c6a44-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6a44-141">-ResourceId</span></span>
<span data-ttu-id="c6a44-142">Строка ресурса ResourceAccessRule ResourceId учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c6a44-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

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

### <span data-ttu-id="c6a44-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="c6a44-143">-TenantId</span></span>
<span data-ttu-id="c6a44-144">Строка " ResourceAccessRule TenantId" учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c6a44-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

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

### <span data-ttu-id="c6a44-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="c6a44-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="c6a44-146">Массив VirtualNetworkResourceId удаляет VirtualNetworkRule с тем же значением VirtualNetworkResourceId из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="c6a44-146">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="c6a44-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c6a44-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="c6a44-148">Массив объектов VirtualNetworkRule, удаляемых из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="c6a44-148">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="c6a44-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6a44-149">-Confirm</span></span>
<span data-ttu-id="c6a44-150">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6a44-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6a44-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6a44-151">-WhatIf</span></span>
<span data-ttu-id="c6a44-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6a44-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6a44-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c6a44-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6a44-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6a44-154">CommonParameters</span></span>
<span data-ttu-id="c6a44-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6a44-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6a44-156">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6a44-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6a44-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6a44-157">INPUTS</span></span>

### <span data-ttu-id="c6a44-158">System.String</span><span class="sxs-lookup"><span data-stu-id="c6a44-158">System.String</span></span>

### <span data-ttu-id="c6a44-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="c6a44-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="c6a44-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="c6a44-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="c6a44-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6a44-161">OUTPUTS</span></span>

### <span data-ttu-id="c6a44-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c6a44-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="c6a44-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="c6a44-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="c6a44-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c6a44-164">NOTES</span></span>

## <span data-ttu-id="c6a44-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6a44-165">RELATED LINKS</span></span>
