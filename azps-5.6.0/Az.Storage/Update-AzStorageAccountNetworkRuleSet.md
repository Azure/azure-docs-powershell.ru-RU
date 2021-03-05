---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 03e6169a9e69b9f2faa3dfaccba934428f7db4e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973288"
---
# <span data-ttu-id="498fe-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="498fe-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="498fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="498fe-102">SYNOPSIS</span></span>
<span data-ttu-id="498fe-103">Обновление свойства NetworkRule учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="498fe-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="498fe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="498fe-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-ResourceAccessRule <PSResourceAccessRule[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="498fe-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="498fe-105">DESCRIPTION</span></span>
<span data-ttu-id="498fe-106">Командлет **Update-AzStorageAccountNetworkRuleSet** обновляет свойство NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="498fe-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="498fe-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="498fe-107">EXAMPLES</span></span>

### <span data-ttu-id="498fe-108">Пример 1. Обновление всех свойств NetworkRule и правила ввода с помощью JSON</span><span class="sxs-lookup"><span data-stu-id="498fe-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"}) -ResourceAccessRule (@{ResourceId=$ResourceId1;TenantId=$tenantId1},@{ResourceId=$ResourceId2;TenantId=$tenantId1})
```

<span data-ttu-id="498fe-109">Эта команда обновляет все свойства NetworkRule и правила ввода с помощью JSON.</span><span class="sxs-lookup"><span data-stu-id="498fe-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="498fe-110">Пример 2. Свойство NetworkRule "Обход обновления"</span><span class="sxs-lookup"><span data-stu-id="498fe-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="498fe-111">Это свойство "Обход команд" NetworkRule (другие свойства не изменяются).</span><span class="sxs-lookup"><span data-stu-id="498fe-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="498fe-112">Пример 3. Очистка правил NetworkRule для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="498fe-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @() -ResourceAccessRule @()
```

<span data-ttu-id="498fe-113">Эта команда очищает правила NetworkRule для учетной записи хранения (другие свойства не изменяются).</span><span class="sxs-lookup"><span data-stu-id="498fe-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="498fe-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="498fe-114">PARAMETERS</span></span>

### <span data-ttu-id="498fe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="498fe-115">-AsJob</span></span>
<span data-ttu-id="498fe-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="498fe-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="498fe-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="498fe-117">-Bypass</span></span>
<span data-ttu-id="498fe-118">Значение Bypass, обновляемого в свойстве NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="498fe-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="498fe-119">Допустимые значения не являются одним или любым сочетанием: • Logging • Метрики • Azureservices</span><span class="sxs-lookup"><span data-stu-id="498fe-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498fe-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="498fe-120">-DefaultAction</span></span>
<span data-ttu-id="498fe-121">Значение DefaultAction, обновляемого в свойстве NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="498fe-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="498fe-122">Разрешенные параметры: • Разрешить • Запретить</span><span class="sxs-lookup"><span data-stu-id="498fe-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="498fe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="498fe-123">-DefaultProfile</span></span>
<span data-ttu-id="498fe-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="498fe-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="498fe-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="498fe-125">-IPRule</span></span>
<span data-ttu-id="498fe-126">Массив ipRule объектов, обновляемого в свойстве NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="498fe-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="498fe-127">-Name</span><span class="sxs-lookup"><span data-stu-id="498fe-127">-Name</span></span>
<span data-ttu-id="498fe-128">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="498fe-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="498fe-129">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="498fe-129">-ResourceAccessRule</span></span>
<span data-ttu-id="498fe-130">NetworkRule ResourceAccessRules для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="498fe-130">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="498fe-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="498fe-131">-ResourceGroupName</span></span>
<span data-ttu-id="498fe-132">Имя группы ресурсов содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="498fe-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="498fe-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="498fe-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="498fe-134">Массив объектов VirtualNetworkRule для обновления до свойства NetworkRule учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="498fe-134">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="498fe-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="498fe-135">-Confirm</span></span>
<span data-ttu-id="498fe-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="498fe-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="498fe-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="498fe-137">-WhatIf</span></span>
<span data-ttu-id="498fe-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="498fe-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="498fe-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="498fe-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="498fe-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="498fe-140">CommonParameters</span></span>
<span data-ttu-id="498fe-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="498fe-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="498fe-142">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="498fe-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="498fe-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="498fe-143">INPUTS</span></span>

### <span data-ttu-id="498fe-144">System.String</span><span class="sxs-lookup"><span data-stu-id="498fe-144">System.String</span></span>

### <span data-ttu-id="498fe-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="498fe-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="498fe-146">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="498fe-146">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="498fe-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="498fe-147">OUTPUTS</span></span>

### <span data-ttu-id="498fe-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="498fe-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="498fe-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="498fe-149">NOTES</span></span>

## <span data-ttu-id="498fe-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="498fe-150">RELATED LINKS</span></span>
