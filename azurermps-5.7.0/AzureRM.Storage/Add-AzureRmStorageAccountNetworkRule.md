---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: b6ec1908af93642cf064b72b1a78a64641749409
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558759"
---
# <span data-ttu-id="953d7-101">Add-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="953d7-101">Add-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="953d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="953d7-102">SYNOPSIS</span></span>
 <span data-ttu-id="953d7-103">Добавление IpRules или VirtualNetworkRules в свойство NetworkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="953d7-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="953d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="953d7-104">SYNTAX</span></span>

### <span data-ttu-id="953d7-105">NetWorkRuleString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="953d7-105">NetWorkRuleString (Default)</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="953d7-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="953d7-106">IpRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="953d7-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="953d7-107">NetworkRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="953d7-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="953d7-108">IpRuleString</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="953d7-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="953d7-109">DESCRIPTION</span></span>
<span data-ttu-id="953d7-110">Командлет **Add-AzureRmStorageAccountNetworkRule** добавляет IpRules или VirtualNetworkRules в свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="953d7-110">The **Add-AzureRmStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="953d7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="953d7-111">EXAMPLES</span></span>

### <span data-ttu-id="953d7-112">Пример 1: Добавление нескольких IpRules с помощью IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="953d7-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="953d7-113">Эта команда добавляет несколько IpRules с IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="953d7-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="953d7-114">Пример 2: Добавление VirtualNetworkRule с VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="953d7-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="953d7-115">Эта команда добавляет VirtualNetworkRule с VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="953d7-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="953d7-116">Пример 3: Добавление VirtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи</span><span class="sxs-lookup"><span data-stu-id="953d7-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="953d7-117">Эта команда добавляет VirtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="953d7-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="953d7-118">Пример 4: Добавление нескольких IpRule с помощью объектов IpRule, ввод с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="953d7-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="953d7-119">Эта команда добавляет несколько IpRule с объектами IpRule, введенными с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="953d7-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="953d7-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="953d7-120">PARAMETERS</span></span>

### <span data-ttu-id="953d7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="953d7-121">-AsJob</span></span>
<span data-ttu-id="953d7-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="953d7-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953d7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="953d7-123">-DefaultProfile</span></span>
<span data-ttu-id="953d7-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="953d7-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953d7-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="953d7-125">-IPAddressOrRange</span></span>
<span data-ttu-id="953d7-126">Массив IpAddressOrRange добавьте IpRules с входными IpAddressOrRange и действием по умолчанию, допускающим NetworkRule свойство.</span><span class="sxs-lookup"><span data-stu-id="953d7-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

```yaml
Type: String[]
Parameter Sets: IpRuleString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953d7-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="953d7-127">-IPRule</span></span>
<span data-ttu-id="953d7-128">Массив объектов IpRule, которые нужно добавить в свойство NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="953d7-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: PSIpRule[]
Parameter Sets: IpRuleObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="953d7-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="953d7-129">-Name</span></span>
<span data-ttu-id="953d7-130">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="953d7-130">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953d7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="953d7-131">-ResourceGroupName</span></span>
<span data-ttu-id="953d7-132">Указывает, что имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="953d7-132">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953d7-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="953d7-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="953d7-134">Массив VirtualNetworkResourceId добавит VirtualNetworkRule с входными VirtualNetworkResourceId и действием по умолчанию, допускающим NetworkRule свойство.</span><span class="sxs-lookup"><span data-stu-id="953d7-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

```yaml
Type: String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953d7-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="953d7-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="953d7-136">Массив объектов VirtualNetworkRule, которые нужно добавить в свойство NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="953d7-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="953d7-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="953d7-137">-Confirm</span></span>
<span data-ttu-id="953d7-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="953d7-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953d7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="953d7-139">-WhatIf</span></span>
<span data-ttu-id="953d7-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="953d7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="953d7-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="953d7-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="953d7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953d7-142">CommonParameters</span></span>
<span data-ttu-id="953d7-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="953d7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="953d7-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="953d7-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953d7-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="953d7-145">INPUTS</span></span>

### <span data-ttu-id="953d7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="953d7-146">System.String</span></span>
<span data-ttu-id="953d7-147">Microsoft. Azure. Commands. Management. Storage. Azure. Commands. PSIpRule. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="953d7-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="953d7-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="953d7-148">OUTPUTS</span></span>

### <span data-ttu-id="953d7-149">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="953d7-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="953d7-150">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="953d7-150">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="953d7-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="953d7-151">NOTES</span></span>

## <span data-ttu-id="953d7-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="953d7-152">RELATED LINKS</span></span>

