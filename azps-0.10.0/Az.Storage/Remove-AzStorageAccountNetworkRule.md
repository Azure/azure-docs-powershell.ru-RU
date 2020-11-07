---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 7823594993dbf2d276f87136c3909ffe88a85918
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910702"
---
# <span data-ttu-id="b56ad-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b56ad-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="b56ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b56ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b56ad-103">Удаление IpRules или VirtualNetworkRules из свойства NetWorkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b56ad-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="b56ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b56ad-104">SYNTAX</span></span>

### <span data-ttu-id="b56ad-105">NetWorkRuleString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b56ad-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b56ad-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="b56ad-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b56ad-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="b56ad-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b56ad-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="b56ad-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b56ad-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b56ad-109">DESCRIPTION</span></span>
<span data-ttu-id="b56ad-110">Командлет **Remove-AzStorageAccountNetworkRule** удаляет IpRules или VirtualNetworkRules из свойства NetWorkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b56ad-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="b56ad-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b56ad-111">EXAMPLES</span></span>

### <span data-ttu-id="b56ad-112">Пример 1: удаление нескольких IpRules с помощью IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b56ad-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="b56ad-113">Эта команда удаляет несколько IpRules с IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="b56ad-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="b56ad-114">Пример 2: удаление VirtualNetworkRule с помощью входного объекта VirtualNetworkRule с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="b56ad-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="b56ad-115">Эта команда удаляет VirtualNetworkRule с VirtualNetworkRule объекта с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="b56ad-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="b56ad-116">Пример 3: удаление первого IpRule с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="b56ad-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="b56ad-117">Эта команда удаляет первый IpRule с конвейером.</span><span class="sxs-lookup"><span data-stu-id="b56ad-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="b56ad-118">Пример 4: удаление нескольких VirtualNetworkRules с помощью VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="b56ad-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="b56ad-119">Эта команда удаляет несколько VirtualNetworkRules с VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="b56ad-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="b56ad-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b56ad-120">PARAMETERS</span></span>

### <span data-ttu-id="b56ad-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b56ad-121">-AsJob</span></span>
<span data-ttu-id="b56ad-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b56ad-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b56ad-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b56ad-123">-DefaultProfile</span></span>
<span data-ttu-id="b56ad-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b56ad-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56ad-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="b56ad-125">-IPAddressOrRange</span></span>
<span data-ttu-id="b56ad-126">Массив IpAddressOrRange удалит IpRule с тем же IpAddressOrRange из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="b56ad-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="b56ad-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="b56ad-127">-IPRule</span></span>
<span data-ttu-id="b56ad-128">Массив объектов IpRule, которые нужно удалить из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="b56ad-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="b56ad-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b56ad-129">-Name</span></span>
<span data-ttu-id="b56ad-130">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b56ad-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="b56ad-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b56ad-131">-ResourceGroupName</span></span>
<span data-ttu-id="b56ad-132">Указывает, что имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="b56ad-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="b56ad-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="b56ad-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="b56ad-134">Массив VirtualNetworkResourceId удалит VirtualNetworkRule с тем же VirtualNetworkResourceId из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="b56ad-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="b56ad-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b56ad-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="b56ad-136">Массив объектов VirtualNetworkRule, которые нужно удалить из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="b56ad-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="b56ad-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b56ad-137">-Confirm</span></span>
<span data-ttu-id="b56ad-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b56ad-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b56ad-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b56ad-139">-WhatIf</span></span>
<span data-ttu-id="b56ad-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b56ad-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b56ad-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b56ad-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b56ad-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56ad-142">CommonParameters</span></span>
<span data-ttu-id="b56ad-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b56ad-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56ad-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b56ad-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56ad-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b56ad-145">INPUTS</span></span>

### <span data-ttu-id="b56ad-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b56ad-146">System.String</span></span>

### <span data-ttu-id="b56ad-147">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="b56ad-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="b56ad-148">Параметры: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b56ad-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="b56ad-149">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="b56ad-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="b56ad-150">Параметры: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b56ad-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="b56ad-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b56ad-151">OUTPUTS</span></span>

### <span data-ttu-id="b56ad-152">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b56ad-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="b56ad-153">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="b56ad-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="b56ad-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="b56ad-154">NOTES</span></span>

## <span data-ttu-id="b56ad-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b56ad-155">RELATED LINKS</span></span>
