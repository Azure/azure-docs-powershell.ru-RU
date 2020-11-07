---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: abfd6f06a0d3f81c84f79e4a5fa6870ad60ba18d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733089"
---
# <span data-ttu-id="2987e-101">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2987e-101">Remove-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="2987e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2987e-102">SYNOPSIS</span></span>
<span data-ttu-id="2987e-103">Удаление IpRules или VirtualNetworkRules из свойства NetWorkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="2987e-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2987e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2987e-104">SYNTAX</span></span>

### <span data-ttu-id="2987e-105">NetWorkRuleString (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2987e-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2987e-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="2987e-106">IpRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2987e-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="2987e-107">NetworkRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2987e-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="2987e-108">IpRuleString</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2987e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2987e-109">DESCRIPTION</span></span>
<span data-ttu-id="2987e-110">Командлет **Remove-AzureRmStorageAccountNetworkRule** удаляет IpRules или VirtualNetworkRules из свойства NetWorkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="2987e-110">The **Remove-AzureRmStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage Account</span></span>

## <span data-ttu-id="2987e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2987e-111">EXAMPLES</span></span>

### <span data-ttu-id="2987e-112">Пример 1: удаление нескольких IpRules с помощью IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2987e-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="2987e-113">Эта команда удаляет несколько IpRules с IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="2987e-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="2987e-114">Пример 2: удаление VirtualNetworkRule с помощью входного объекта VirtualNetworkRule с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="2987e-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="2987e-115">Эта команда удаляет VirtualNetworkRule с VirtualNetworkRule объекта с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="2987e-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="2987e-116">Пример 3: удаление первого IpRule с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="2987e-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount").IpRules[0] | Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="2987e-117">Эта команда удаляет первый IpRule с конвейером.</span><span class="sxs-lookup"><span data-stu-id="2987e-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="2987e-118">Пример 4: удаление нескольких VirtualNetworkRules с помощью VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="2987e-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="2987e-119">Эта команда удаляет несколько VirtualNetworkRules с VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="2987e-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="2987e-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2987e-120">PARAMETERS</span></span>

### <span data-ttu-id="2987e-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2987e-121">-IPAddressOrRange</span></span>
<span data-ttu-id="2987e-122">Массив IpAddressOrRange удалит IpRule с тем же IpAddressOrRange из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="2987e-122">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="2987e-123">-IPRule</span><span class="sxs-lookup"><span data-stu-id="2987e-123">-IPRule</span></span>
<span data-ttu-id="2987e-124">Массив объектов IpRule, которые нужно удалить из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="2987e-124">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="2987e-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2987e-125">-Name</span></span>
<span data-ttu-id="2987e-126">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2987e-126">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="2987e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2987e-127">-ResourceGroupName</span></span>
<span data-ttu-id="2987e-128">Указывает, что имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="2987e-128">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="2987e-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="2987e-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="2987e-130">Массив VirtualNetworkResourceId удалит VirtualNetworkRule с тем же VirtualNetworkResourceId из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="2987e-130">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="2987e-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2987e-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="2987e-132">Массив объектов VirtualNetworkRule, которые нужно удалить из свойства NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="2987e-132">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="2987e-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2987e-133">-Confirm</span></span>
<span data-ttu-id="2987e-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2987e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2987e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2987e-135">-WhatIf</span></span>
<span data-ttu-id="2987e-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2987e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2987e-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2987e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2987e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2987e-138">-DefaultProfile</span></span>
<span data-ttu-id="2987e-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2987e-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2987e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2987e-140">CommonParameters</span></span>
<span data-ttu-id="2987e-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2987e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2987e-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2987e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2987e-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2987e-143">INPUTS</span></span>

### <span data-ttu-id="2987e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="2987e-144">System.String</span></span>
<span data-ttu-id="2987e-145">Microsoft. Azure. Commands. Management. Storage. Azure. Commands. PSIpRule. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="2987e-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="2987e-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2987e-146">OUTPUTS</span></span>

### <span data-ttu-id="2987e-147">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="2987e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="2987e-148">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="2987e-148">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="2987e-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="2987e-149">NOTES</span></span>

## <span data-ttu-id="2987e-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2987e-150">RELATED LINKS</span></span>

