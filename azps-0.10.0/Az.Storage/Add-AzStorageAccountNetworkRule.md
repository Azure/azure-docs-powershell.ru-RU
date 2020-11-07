---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: fb8df6e3444a650cc5f3c249545a43b4033689bd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910796"
---
# <span data-ttu-id="c08bc-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c08bc-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="c08bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c08bc-102">SYNOPSIS</span></span>
 <span data-ttu-id="c08bc-103">Добавление IpRules или VirtualNetworkRules в свойство NetworkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="c08bc-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="c08bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c08bc-104">SYNTAX</span></span>

### <span data-ttu-id="c08bc-105">NetWorkRuleString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c08bc-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c08bc-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="c08bc-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c08bc-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="c08bc-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c08bc-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="c08bc-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c08bc-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c08bc-109">DESCRIPTION</span></span>
<span data-ttu-id="c08bc-110">Командлет **Add-AzStorageAccountNetworkRule** добавляет IpRules или VirtualNetworkRules в свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c08bc-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="c08bc-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c08bc-111">EXAMPLES</span></span>

### <span data-ttu-id="c08bc-112">Пример 1: Добавление нескольких IpRules с помощью IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c08bc-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="c08bc-113">Эта команда добавляет несколько IpRules с IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="c08bc-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="c08bc-114">Пример 2: Добавление VirtualNetworkRule с VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="c08bc-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="c08bc-115">Эта команда добавляет VirtualNetworkRule с VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="c08bc-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="c08bc-116">Пример 3: Добавление VirtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи</span><span class="sxs-lookup"><span data-stu-id="c08bc-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="c08bc-117">Эта команда добавляет VirtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c08bc-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="c08bc-118">Пример 4: Добавление нескольких IpRule с помощью объектов IpRule, ввод с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="c08bc-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="c08bc-119">Эта команда добавляет несколько IpRule с объектами IpRule, введенными с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="c08bc-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="c08bc-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c08bc-120">PARAMETERS</span></span>

### <span data-ttu-id="c08bc-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c08bc-121">-AsJob</span></span>
<span data-ttu-id="c08bc-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c08bc-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c08bc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c08bc-123">-DefaultProfile</span></span>
<span data-ttu-id="c08bc-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c08bc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c08bc-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="c08bc-125">-IPAddressOrRange</span></span>
<span data-ttu-id="c08bc-126">Массив IpAddressOrRange добавьте IpRules с входными IpAddressOrRange и действием по умолчанию, допускающим NetworkRule свойство.</span><span class="sxs-lookup"><span data-stu-id="c08bc-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="c08bc-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="c08bc-127">-IPRule</span></span>
<span data-ttu-id="c08bc-128">Массив объектов IpRule, которые нужно добавить в свойство NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="c08bc-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="c08bc-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c08bc-129">-Name</span></span>
<span data-ttu-id="c08bc-130">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c08bc-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="c08bc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c08bc-131">-ResourceGroupName</span></span>
<span data-ttu-id="c08bc-132">Указывает, что имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="c08bc-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="c08bc-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="c08bc-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="c08bc-134">Массив VirtualNetworkResourceId добавит VirtualNetworkRule с входными VirtualNetworkResourceId и действием по умолчанию, допускающим NetworkRule свойство.</span><span class="sxs-lookup"><span data-stu-id="c08bc-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="c08bc-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c08bc-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="c08bc-136">Массив объектов VirtualNetworkRule, которые нужно добавить в свойство NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="c08bc-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="c08bc-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c08bc-137">-Confirm</span></span>
<span data-ttu-id="c08bc-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c08bc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c08bc-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c08bc-139">-WhatIf</span></span>
<span data-ttu-id="c08bc-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c08bc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c08bc-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c08bc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c08bc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c08bc-142">CommonParameters</span></span>
<span data-ttu-id="c08bc-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c08bc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c08bc-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c08bc-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c08bc-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c08bc-145">INPUTS</span></span>

### <span data-ttu-id="c08bc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c08bc-146">System.String</span></span>

### <span data-ttu-id="c08bc-147">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="c08bc-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="c08bc-148">Параметры: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c08bc-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="c08bc-149">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="c08bc-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="c08bc-150">Параметры: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c08bc-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="c08bc-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c08bc-151">OUTPUTS</span></span>

### <span data-ttu-id="c08bc-152">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c08bc-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="c08bc-153">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="c08bc-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="c08bc-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="c08bc-154">NOTES</span></span>

## <span data-ttu-id="c08bc-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c08bc-155">RELATED LINKS</span></span>
