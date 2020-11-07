---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 0fb90529f4157bf627e43477e3db41764040e5c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732940"
---
# <span data-ttu-id="c1c51-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="c1c51-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="c1c51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1c51-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c51-103">Создает пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="c1c51-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1c51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1c51-104">SYNTAX</span></span>

### <span data-ttu-id="c1c51-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c1c51-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1c51-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c1c51-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1c51-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1c51-107">DESCRIPTION</span></span>
<span data-ttu-id="c1c51-108">Командлет New-AzureRmEventHubNamespace создает новое пространство имен концентраторов событий типа.</span><span class="sxs-lookup"><span data-stu-id="c1c51-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="c1c51-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1c51-109">EXAMPLES</span></span>

### <span data-ttu-id="c1c51-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c1c51-110">Example 1</span></span>                                              
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="c1c51-111">Создает пространство имен MyNamespaceNameных концентраторов событий \` \` в указанном географическом расположении \` MyLocation \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c1c51-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c1c51-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c1c51-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="c1c51-113">Создает пространство имен концентраторов \` событий \` , MyNamespaceName в указанном географическом расположении \` MyLocation \` , в группе ресурсов \` MyResourceGroupName \` и AutoInflate включено с MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="c1c51-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="c1c51-114">Пример 3-Kafka Enabled Namespace</span><span class="sxs-lookup"><span data-stu-id="c1c51-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka
```

<span data-ttu-id="c1c51-115">Создает пространство имен концентраторов \` событий \` , MyNamespaceName в указанном географическом расположении \` MyLocation \` , в группе ресурсов \` MyResourceGroupName \` с Kafka и AutoInflate.</span><span class="sxs-lookup"><span data-stu-id="c1c51-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="c1c51-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1c51-116">PARAMETERS</span></span>

### <span data-ttu-id="c1c51-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c51-117">-DefaultProfile</span></span>
<span data-ttu-id="c1c51-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1c51-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1c51-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="c1c51-119">-EnableAutoInflate</span></span>
<span data-ttu-id="c1c51-120">Указывает, включена ли AutoInflate</span><span class="sxs-lookup"><span data-stu-id="c1c51-120">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1c51-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="c1c51-121">-EnableKafka</span></span>
<span data-ttu-id="c1c51-122">Включение и отключение Kafka для пространства имен</span><span class="sxs-lookup"><span data-stu-id="c1c51-122">enabling or disabling Kafka for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```         

### <span data-ttu-id="c1c51-123">-Location</span><span class="sxs-lookup"><span data-stu-id="c1c51-123">-Location</span></span>
<span data-ttu-id="c1c51-124">Расположение пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="c1c51-124">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c51-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="c1c51-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="c1c51-126">Верхний предел количества единиц пропускной способности при включенном AutoInflate значение должно находиться в диапазоне от 0 до 20 единиц пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="c1c51-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c51-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1c51-127">-Name</span></span>
<span data-ttu-id="c1c51-128">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="c1c51-128">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c51-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1c51-129">-ResourceGroupName</span></span>
<span data-ttu-id="c1c51-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c1c51-130">Resource Group Name</span></span>

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

### <span data-ttu-id="c1c51-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c1c51-131">-SkuCapacity</span></span>
<span data-ttu-id="c1c51-132">Единицы пропускной способности eventhub.</span><span class="sxs-lookup"><span data-stu-id="c1c51-132">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c51-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c1c51-133">-SkuName</span></span>
<span data-ttu-id="c1c51-134">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c1c51-134">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c51-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="c1c51-135">-Tag</span></span>
<span data-ttu-id="c1c51-136">Хэш-таблицы, представляющие Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c1c51-136">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c51-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1c51-137">-Confirm</span></span>
<span data-ttu-id="c1c51-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c1c51-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1c51-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1c51-139">-WhatIf</span></span>
<span data-ttu-id="c1c51-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c1c51-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1c51-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c1c51-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1c51-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c51-142">CommonParameters</span></span>
<span data-ttu-id="c1c51-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1c51-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c1c51-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1c51-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c51-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1c51-145">INPUTS</span></span>


## <span data-ttu-id="c1c51-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1c51-146">OUTPUTS</span></span>

### <span data-ttu-id="c1c51-147">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c1c51-147">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="c1c51-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1c51-148">NOTES</span></span>

## <span data-ttu-id="c1c51-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1c51-149">RELATED LINKS</span></span>
