---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/6911f050bfba3248a3fd992fbc2645e3a1a8641d
ms.openlocfilehash: 05f0c3cd3947a1955689a7359b40d59052863ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559815"
---
# <span data-ttu-id="4db08-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="4db08-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="4db08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4db08-102">SYNOPSIS</span></span>
<span data-ttu-id="4db08-103">Обновляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="4db08-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4db08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4db08-104">SYNTAX</span></span>

### <span data-ttu-id="4db08-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4db08-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4db08-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="4db08-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="4db08-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4db08-107">DESCRIPTION</span></span>
<span data-ttu-id="4db08-108">Командлет Set-AzureRmEventHubNamespace обновляет свойства указанного пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="4db08-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="4db08-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4db08-109">EXAMPLES</span></span>

### <span data-ttu-id="4db08-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4db08-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="4db08-111">Обновляет состояние пространства имен \` MyNamespaceName \` для создания.</span><span class="sxs-lookup"><span data-stu-id="4db08-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="4db08-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4db08-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="4db08-113">Обновляет состояние пространства имен \` MyNamespaceName \` с AutoInflate = Enabled и MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="4db08-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="4db08-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4db08-114">PARAMETERS</span></span>

### <span data-ttu-id="4db08-115">-Location</span><span class="sxs-lookup"><span data-stu-id="4db08-115">-Location</span></span>
<span data-ttu-id="4db08-116">Географическое расположение пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="4db08-116">Event Hubs namespace geo-location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db08-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4db08-117">-ResourceGroupName</span></span>
<span data-ttu-id="4db08-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4db08-118">Resource group name.</span></span>

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

### <span data-ttu-id="4db08-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4db08-119">-SkuCapacity</span></span>
<span data-ttu-id="4db08-120">Единицы пропускной способности концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="4db08-120">The Event Hub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db08-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4db08-121">-SkuName</span></span>
<span data-ttu-id="4db08-122">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4db08-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db08-123">-State</span><span class="sxs-lookup"><span data-stu-id="4db08-123">-State</span></span>
<span data-ttu-id="4db08-124">Задает состояние (отключено или включено) пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4db08-124">Specifies the state (disabled or enabled) of the namespace.</span></span>

```yaml
Type: NamespaceState
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, Creating, Created, Activating, Enabling, Active, Disabling, Disabled, SoftDeleting, SoftDeleted, Removing, Removed, Failed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db08-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="4db08-125">-Tag</span></span>
<span data-ttu-id="4db08-126">Хэш-таблицы, представляющие Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4db08-126">Hashtables that represent resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db08-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4db08-127">-Confirm</span></span>
<span data-ttu-id="4db08-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4db08-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db08-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4db08-129">-WhatIf</span></span>
<span data-ttu-id="4db08-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4db08-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4db08-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4db08-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db08-132">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="4db08-132">-EnableAutoInflate</span></span>
<span data-ttu-id="4db08-133">Указывает, включена ли AutoInflate</span><span class="sxs-lookup"><span data-stu-id="4db08-133">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NamespaceParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db08-134">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="4db08-134">-MaximumThroughputUnits</span></span>
<span data-ttu-id="4db08-135">Верхний предел количества единиц пропускной способности при включенном AutoInflate значение vaule должно быть в пределах от 0 до 20 единиц пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="4db08-135">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4db08-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4db08-136">-Name</span></span>
<span data-ttu-id="4db08-137">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="4db08-137">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="4db08-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4db08-138">INPUTS</span></span>

### <span data-ttu-id="4db08-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4db08-139">System.String</span></span>

### <span data-ttu-id="4db08-140">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4db08-140">System.Int32</span></span>

### <span data-ttu-id="4db08-141">Microsoft. Azure. Management. EventHub. Models. NamespaceState</span><span class="sxs-lookup"><span data-stu-id="4db08-141">Microsoft.Azure.Management.EventHub.Models.NamespaceState</span></span>

### <span data-ttu-id="4db08-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4db08-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4db08-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4db08-143">OUTPUTS</span></span>

### <span data-ttu-id="4db08-144">Microsoft. Azure. Commands. EventHub. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="4db08-144">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="4db08-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="4db08-145">NOTES</span></span>

## <span data-ttu-id="4db08-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4db08-146">RELATED LINKS</span></span>

