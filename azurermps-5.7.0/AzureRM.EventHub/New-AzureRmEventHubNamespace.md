---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubNamespace.md
ms.openlocfilehash: 2d944b629a72a8b97bf1bd639ced79d9bd1eab02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566630"
---
# <span data-ttu-id="c7a8c-101">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="c7a8c-101">New-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="c7a8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7a8c-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a8c-103">Создает пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-103">Creates an Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7a8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7a8c-104">SYNTAX</span></span>

### <span data-ttu-id="c7a8c-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7a8c-105">NamespaceParameterSet (Default)</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7a8c-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7a8c-106">AutoInflateParameterSet</span></span>
```
New-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7a8c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7a8c-107">DESCRIPTION</span></span>
<span data-ttu-id="c7a8c-108">Командлет New-AzureRmEventHubNamespace создает новое пространство имен концентраторов событий типа.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-108">The New-AzureRmEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="c7a8c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7a8c-109">EXAMPLES</span></span>

### <span data-ttu-id="c7a8c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7a8c-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation
```

<span data-ttu-id="c7a8c-111">Создает пространство имен MyNamespaceNameных концентраторов событий \` \` в указанном географическом расположении \` MyLocation \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c7a8c-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c7a8c-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c7a8c-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="c7a8c-113">Создает пространство имен концентраторов \` событий \` , MyNamespaceName в указанном географическом расположении \` MyLocation \` , в группе ресурсов \` MyResourceGroupName \` и AutoInflate включено с MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

## <span data-ttu-id="c7a8c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7a8c-114">PARAMETERS</span></span>

### <span data-ttu-id="c7a8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a8c-115">-DefaultProfile</span></span>
<span data-ttu-id="c7a8c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7a8c-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="c7a8c-117">-EnableAutoInflate</span></span>
<span data-ttu-id="c7a8c-118">Указывает, включена ли AutoInflate</span><span class="sxs-lookup"><span data-stu-id="c7a8c-118">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7a8c-119">-Location</span><span class="sxs-lookup"><span data-stu-id="c7a8c-119">-Location</span></span>
<span data-ttu-id="c7a8c-120">Расположение пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="c7a8c-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="c7a8c-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="c7a8c-122">Верхний предел количества единиц пропускной способности при включенном AutoInflate значение должно находиться в диапазоне от 0 до 20 единиц пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a8c-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7a8c-123">-Name</span></span>
<span data-ttu-id="c7a8c-124">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-124">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a8c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a8c-125">-ResourceGroupName</span></span>
<span data-ttu-id="c7a8c-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c7a8c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="c7a8c-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c7a8c-127">-SkuCapacity</span></span>
<span data-ttu-id="c7a8c-128">Единицы пропускной способности eventhub.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-128">The eventhub throughput units.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a8c-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c7a8c-129">-SkuName</span></span>
<span data-ttu-id="c7a8c-130">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="c7a8c-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="c7a8c-131">-Tag</span></span>
<span data-ttu-id="c7a8c-132">Хэш-таблицы, представляющие Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-132">Hashtables which represents resource Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7a8c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7a8c-133">-Confirm</span></span>
<span data-ttu-id="c7a8c-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7a8c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7a8c-135">-WhatIf</span></span>
<span data-ttu-id="c7a8c-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7a8c-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7a8c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a8c-138">CommonParameters</span></span>
<span data-ttu-id="c7a8c-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7a8c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c7a8c-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a8c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a8c-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7a8c-141">INPUTS</span></span>

### <span data-ttu-id="c7a8c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c7a8c-142">System.String</span></span>
<span data-ttu-id="c7a8c-143">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]] System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c7a8c-143">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]] System.Collections.Hashtable</span></span>


## <span data-ttu-id="c7a8c-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7a8c-144">OUTPUTS</span></span>

### <span data-ttu-id="c7a8c-145">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="c7a8c-145">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>


## <span data-ttu-id="c7a8c-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7a8c-146">NOTES</span></span>

## <span data-ttu-id="c7a8c-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7a8c-147">RELATED LINKS</span></span>
