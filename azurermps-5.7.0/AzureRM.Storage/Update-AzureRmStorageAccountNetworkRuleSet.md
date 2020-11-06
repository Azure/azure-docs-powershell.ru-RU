---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 8851f7e2820e1c9a0a63b475544c49fe5c0c8ee7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567365"
---
# <span data-ttu-id="9eecb-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9eecb-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="9eecb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9eecb-102">SYNOPSIS</span></span>
<span data-ttu-id="9eecb-103">Обновление свойства NetworkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9eecb-103">Update the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9eecb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9eecb-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eecb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9eecb-105">DESCRIPTION</span></span>
<span data-ttu-id="9eecb-106">Командлет **Update-AzureRmStorageAccountNetworkRuleSet** обновляет свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9eecb-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="9eecb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9eecb-107">EXAMPLES</span></span>

### <span data-ttu-id="9eecb-108">Пример 1: обновление всех свойств NetworkRule, правил ввода с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="9eecb-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="9eecb-109">Эта команда обновляет все свойства NetworkRule, правила ввода с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="9eecb-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="9eecb-110">Пример 2: обновление свойства обхода для NetworkRule</span><span class="sxs-lookup"><span data-stu-id="9eecb-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="9eecb-111">Это обновление свойства обхода для NetworkRule (другие свойства не изменяются).</span><span class="sxs-lookup"><span data-stu-id="9eecb-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="9eecb-112">Пример 3: Очистка правил NetworkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9eecb-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="9eecb-113">Эта команда очищает правила для NetworkRule учетной записи хранения (другие свойства не изменяются).</span><span class="sxs-lookup"><span data-stu-id="9eecb-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="9eecb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9eecb-114">PARAMETERS</span></span>

### <span data-ttu-id="9eecb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9eecb-115">-AsJob</span></span>
<span data-ttu-id="9eecb-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9eecb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9eecb-117">-Обход</span><span class="sxs-lookup"><span data-stu-id="9eecb-117">-Bypass</span></span>
<span data-ttu-id="9eecb-118">Значение пропуска для обновления свойства NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9eecb-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="9eecb-119">Разрешенное значение — None (нет) или любое сочетание: • ведение журнала • метрическая система мер • Azureservices</span><span class="sxs-lookup"><span data-stu-id="9eecb-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

```yaml
Type: PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases: 
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eecb-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="9eecb-120">-DefaultAction</span></span>
<span data-ttu-id="9eecb-121">Значение DefaultAction, которое требуется обновить, на свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9eecb-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="9eecb-122">Разрешенные варианты: • разрешить • запретить</span><span class="sxs-lookup"><span data-stu-id="9eecb-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases: 
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eecb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eecb-123">-DefaultProfile</span></span>
<span data-ttu-id="9eecb-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9eecb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eecb-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="9eecb-125">-IPRule</span></span>
<span data-ttu-id="9eecb-126">Массив объектов IpRule, которые нужно обновить, на свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9eecb-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: PSIpRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eecb-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9eecb-127">-Name</span></span>
<span data-ttu-id="9eecb-128">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9eecb-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="9eecb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eecb-129">-ResourceGroupName</span></span>
<span data-ttu-id="9eecb-130">Указывает, что имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="9eecb-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="9eecb-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9eecb-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="9eecb-132">Массив объектов VirtualNetworkRule, которые нужно обновить, на свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9eecb-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eecb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9eecb-133">-Confirm</span></span>
<span data-ttu-id="9eecb-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9eecb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eecb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eecb-135">-WhatIf</span></span>
<span data-ttu-id="9eecb-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9eecb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eecb-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9eecb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eecb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eecb-138">CommonParameters</span></span>
<span data-ttu-id="9eecb-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9eecb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eecb-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eecb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eecb-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9eecb-141">INPUTS</span></span>

### <span data-ttu-id="9eecb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9eecb-142">System.String</span></span>
<span data-ttu-id="9eecb-143">Microsoft. Azure. Commands. Management. Storage. Azure. Commands. PSIpRule. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="9eecb-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="9eecb-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9eecb-144">OUTPUTS</span></span>

### <span data-ttu-id="9eecb-145">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9eecb-145">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="9eecb-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="9eecb-146">NOTES</span></span>

## <span data-ttu-id="9eecb-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9eecb-147">RELATED LINKS</span></span>

