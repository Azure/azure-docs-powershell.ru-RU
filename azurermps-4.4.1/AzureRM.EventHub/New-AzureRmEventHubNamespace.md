---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 07b5de12e042c81bb5f27c844d1fc8962453310a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734854"
---
# <span data-ttu-id="063f4-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="063f4-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="063f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="063f4-102">SYNOPSIS</span></span>
<span data-ttu-id="063f4-103">Создает пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="063f4-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="063f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="063f4-104">SYNTAX</span></span>

### <span data-ttu-id="063f4-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="063f4-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="063f4-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="063f4-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-EnableAutoInflate]
 [-MaximumThroughputUnits] <Int32> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="063f4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="063f4-107">DESCRIPTION</span></span>
<span data-ttu-id="063f4-108">Командлет New-AzureRmEventHubNamespace создает новое пространство имен концентраторов событий типа.</span><span class="sxs-lookup"><span data-stu-id="063f4-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="063f4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="063f4-109">EXAMPLES</span></span>

### <span data-ttu-id="063f4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="063f4-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation 
```

<span data-ttu-id="063f4-111">Создает пространство имен MyNamespaceNameных концентраторов событий \` \` в указанном географическом расположении \` MyLocation \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="063f4-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="063f4-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="063f4-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="063f4-113">Создает пространство имен концентраторов \` событий \` , MyNamespaceName в указанном географическом расположении \` MyLocation \` , в группе ресурсов \` MyResourceGroupName \` и AutoInflate включено с MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="063f4-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="063f4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="063f4-114">PARAMETERS</span></span>

### <span data-ttu-id="063f4-115">-Location</span><span class="sxs-lookup"><span data-stu-id="063f4-115">-Location</span></span>
<span data-ttu-id="063f4-116">Географическое расположение пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="063f4-116">Event Hubs namespace geo-location.</span></span>

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

### <span data-ttu-id="063f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="063f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="063f4-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="063f4-118">Resource group name.</span></span>

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

### <span data-ttu-id="063f4-119">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="063f4-119">-SkuCapacity</span></span>
<span data-ttu-id="063f4-120">Единицы пропускной способности концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="063f4-120">The Event Hub throughput units.</span></span>

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

### <span data-ttu-id="063f4-121">-SkuName</span><span class="sxs-lookup"><span data-stu-id="063f4-121">-SkuName</span></span>
<span data-ttu-id="063f4-122">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="063f4-122">Namespace Sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="063f4-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="063f4-123">-Tag</span></span>
<span data-ttu-id="063f4-124">Хэш-таблицы, представляющие Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="063f4-124">Hashtables that represent resource tags.</span></span>

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

### <span data-ttu-id="063f4-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="063f4-125">-Confirm</span></span>
<span data-ttu-id="063f4-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="063f4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="063f4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="063f4-127">-WhatIf</span></span>
<span data-ttu-id="063f4-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="063f4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="063f4-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="063f4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="063f4-130">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="063f4-130">-EnableAutoInflate</span></span>
<span data-ttu-id="063f4-131">Указывает, включена ли AutoInflate</span><span class="sxs-lookup"><span data-stu-id="063f4-131">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="063f4-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="063f4-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="063f4-133">Верхний предел количества единиц пропускной способности при включенном AutoInflate значение vaule должно быть в пределах от 0 до 20 единиц пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="063f4-133">Upper limit of throughput units when AutoInflate is enabled, vaule should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="063f4-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="063f4-134">-Name</span></span>
<span data-ttu-id="063f4-135">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="063f4-135">EventHub Namespace Name.</span></span>

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

## <span data-ttu-id="063f4-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="063f4-136">INPUTS</span></span>

### <span data-ttu-id="063f4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="063f4-137">System.String</span></span>
<span data-ttu-id="063f4-138">System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = B77a5c561934e089 \] \] System. Nullable \` 1 \[ \[ System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089 \] \] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="063f4-138">System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Nullable\`1\[\[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\] System.Collections.Hashtable</span></span>

## <span data-ttu-id="063f4-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="063f4-139">OUTPUTS</span></span>

### <span data-ttu-id="063f4-140">Microsoft. Azure. Commands. EventHub. Models. NamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="063f4-140">Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes</span></span>

## <span data-ttu-id="063f4-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="063f4-141">NOTES</span></span>

## <span data-ttu-id="063f4-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="063f4-142">RELATED LINKS</span></span>

