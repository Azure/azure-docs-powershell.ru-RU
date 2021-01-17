---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420132"
---
# <span data-ttu-id="47a08-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="47a08-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="47a08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47a08-102">SYNOPSIS</span></span>
 <span data-ttu-id="47a08-103">Добавление IpRules или VirtualNetworkRules в свойство NetworkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="47a08-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="47a08-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="47a08-104">SYNTAX</span></span>

### <span data-ttu-id="47a08-105">NetWorkRuleString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47a08-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47a08-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="47a08-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47a08-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="47a08-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47a08-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="47a08-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47a08-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47a08-109">DESCRIPTION</span></span>
<span data-ttu-id="47a08-110">Командлет **Add-AzStorageAccountNetworkRule** добавляет IpRules или VirtualNetworkRules к свойству NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="47a08-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="47a08-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="47a08-111">EXAMPLES</span></span>

### <span data-ttu-id="47a08-112">Пример 1. Добавление нескольких IpRules с IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="47a08-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="47a08-113">Эта команда добавляет несколько ipRules с IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="47a08-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="47a08-114">Пример 2. Добавление значения VirtualNetworkRule с помощью VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="47a08-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="47a08-115">Эта команда добавляет virtualNetworkRule с VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="47a08-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="47a08-116">Пример 3. Добавление virtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи</span><span class="sxs-lookup"><span data-stu-id="47a08-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="47a08-117">Эта команда добавляет virtualNetworkRules с объектами VirtualNetworkRule из другой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="47a08-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="47a08-118">Пример 4. Добавление нескольких объектов IpRule с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="47a08-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="47a08-119">Эта команда добавляет несколько объектов IpRule, вводимых с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="47a08-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="47a08-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47a08-120">PARAMETERS</span></span>

### <span data-ttu-id="47a08-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47a08-121">-AsJob</span></span>
<span data-ttu-id="47a08-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="47a08-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47a08-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a08-123">-DefaultProfile</span></span>
<span data-ttu-id="47a08-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47a08-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47a08-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="47a08-125">-IPAddressOrRange</span></span>
<span data-ttu-id="47a08-126">Массив IpAddressOrRange, добавьте IpRules со входным значением IpAddressOrRange и действием по умолчанию Allow to NetworkRule Property.</span><span class="sxs-lookup"><span data-stu-id="47a08-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="47a08-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="47a08-127">-IPRule</span></span>
<span data-ttu-id="47a08-128">Массив объектов IpRule, добавляемого в свойство NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="47a08-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="47a08-129">-Name</span><span class="sxs-lookup"><span data-stu-id="47a08-129">-Name</span></span>
<span data-ttu-id="47a08-130">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="47a08-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="47a08-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47a08-131">-ResourceGroupName</span></span>
<span data-ttu-id="47a08-132">Имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="47a08-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="47a08-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="47a08-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="47a08-134">Массив VirtualNetworkResourceId добавит VirtualNetworkRule со входными данными VirtualNetworkResourceId и действием по умолчанию Allow to NetworkRule Property.</span><span class="sxs-lookup"><span data-stu-id="47a08-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="47a08-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="47a08-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="47a08-136">Массив объектов VirtualNetworkRule, которые нужно добавить в свойство NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="47a08-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="47a08-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47a08-137">-Confirm</span></span>
<span data-ttu-id="47a08-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47a08-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47a08-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47a08-139">-WhatIf</span></span>
<span data-ttu-id="47a08-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47a08-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47a08-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="47a08-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47a08-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a08-142">CommonParameters</span></span>
<span data-ttu-id="47a08-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47a08-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a08-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47a08-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a08-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47a08-145">INPUTS</span></span>

### <span data-ttu-id="47a08-146">System.String</span><span class="sxs-lookup"><span data-stu-id="47a08-146">System.String</span></span>

### <span data-ttu-id="47a08-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="47a08-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="47a08-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="47a08-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="47a08-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="47a08-149">OUTPUTS</span></span>

### <span data-ttu-id="47a08-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="47a08-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="47a08-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="47a08-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="47a08-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="47a08-152">NOTES</span></span>

## <span data-ttu-id="47a08-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47a08-153">RELATED LINKS</span></span>
