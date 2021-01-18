---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 1eeaf3a7c9d0c4b5715bc5b75e42e53a8fa98c5e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505680"
---
# <span data-ttu-id="dbdf3-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dbdf3-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="dbdf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbdf3-102">SYNOPSIS</span></span>
<span data-ttu-id="dbdf3-103">Удаление IpRules или VirtualNetworkRules из свойства NetWorkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="dbdf3-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="dbdf3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dbdf3-104">SYNTAX</span></span>

### <span data-ttu-id="dbdf3-105">NetWorkRuleString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dbdf3-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dbdf3-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="dbdf3-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbdf3-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="dbdf3-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dbdf3-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="dbdf3-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbdf3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbdf3-109">DESCRIPTION</span></span>
<span data-ttu-id="dbdf3-110">Командлет **Remove-AzStorageAccountNetworkRule** удаляет IpRules или VirtualNetworkRules из свойства NetWorkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="dbdf3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dbdf3-111">EXAMPLES</span></span>

### <span data-ttu-id="dbdf3-112">Пример 1. Удаление нескольких IpRules с помощью IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="dbdf3-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="dbdf3-113">Эта команда удаляет несколько ipRules с IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="dbdf3-114">Пример 2. Удаление объекта VirtualNetworkRule с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="dbdf3-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="dbdf3-115">Эта команда удаляет объект VirtualNetworkRule с объектом VirtualNetworkRule, входным с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="dbdf3-116">Пример 3. Удаление первого IpRule с конвейером</span><span class="sxs-lookup"><span data-stu-id="dbdf3-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="dbdf3-117">Эта команда удаляет первое ipRule с конвейером.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="dbdf3-118">Пример 4. Удаление нескольких VirtualNetworkRules с помощью VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="dbdf3-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="dbdf3-119">Эта команда удаляет несколько виртуальныхNetworkRules с virtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="dbdf3-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbdf3-120">PARAMETERS</span></span>

### <span data-ttu-id="dbdf3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbdf3-121">-AsJob</span></span>
<span data-ttu-id="dbdf3-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dbdf3-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dbdf3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbdf3-123">-DefaultProfile</span></span>
<span data-ttu-id="dbdf3-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbdf3-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="dbdf3-125">-IPAddressOrRange</span></span>
<span data-ttu-id="dbdf3-126">Массив IpAddressOrRange удаляет IpRule с тем же ipAddressOrRange из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="dbdf3-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="dbdf3-127">-IPRule</span></span>
<span data-ttu-id="dbdf3-128">Массив объектов IpRule, удаляемого из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="dbdf3-129">-Name</span><span class="sxs-lookup"><span data-stu-id="dbdf3-129">-Name</span></span>
<span data-ttu-id="dbdf3-130">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="dbdf3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbdf3-131">-ResourceGroupName</span></span>
<span data-ttu-id="dbdf3-132">Имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="dbdf3-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="dbdf3-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="dbdf3-134">Массив VirtualNetworkResourceId удаляет VirtualNetworkRule с тем же значением VirtualNetworkResourceId из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="dbdf3-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dbdf3-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="dbdf3-136">Массив объектов VirtualNetworkRule, удаляемых из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="dbdf3-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbdf3-137">-Confirm</span></span>
<span data-ttu-id="dbdf3-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbdf3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbdf3-139">-WhatIf</span></span>
<span data-ttu-id="dbdf3-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbdf3-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbdf3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbdf3-142">CommonParameters</span></span>
<span data-ttu-id="dbdf3-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbdf3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbdf3-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbdf3-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbdf3-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbdf3-145">INPUTS</span></span>

### <span data-ttu-id="dbdf3-146">System.String</span><span class="sxs-lookup"><span data-stu-id="dbdf3-146">System.String</span></span>

### <span data-ttu-id="dbdf3-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="dbdf3-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="dbdf3-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="dbdf3-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="dbdf3-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dbdf3-149">OUTPUTS</span></span>

### <span data-ttu-id="dbdf3-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dbdf3-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="dbdf3-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="dbdf3-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="dbdf3-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dbdf3-152">NOTES</span></span>

## <span data-ttu-id="dbdf3-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbdf3-153">RELATED LINKS</span></span>
