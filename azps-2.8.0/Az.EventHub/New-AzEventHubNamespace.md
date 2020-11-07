---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 9217dfa2d5465841cb0ed33c2781849ddebff3b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720945"
---
# <span data-ttu-id="3ec6f-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="3ec6f-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="3ec6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3ec6f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec6f-103">Создает пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="3ec6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3ec6f-104">SYNTAX</span></span>

### <span data-ttu-id="3ec6f-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3ec6f-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ec6f-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ec6f-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ec6f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ec6f-107">DESCRIPTION</span></span>
<span data-ttu-id="3ec6f-108">Командлет New-AzEventHubNamespace создает новое пространство имен концентраторов событий типа.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="3ec6f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3ec6f-109">EXAMPLES</span></span>

### <span data-ttu-id="3ec6f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ec6f-110">Example 1</span></span>                                           
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : False
MaximumThroughputUnits : 0
```

<span data-ttu-id="3ec6f-111">Создает пространство имен MyNamespaceNameных концентраторов событий \` \` в указанном географическом расположении \` MyLocation \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="3ec6f-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3ec6f-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3ec6f-112">Example 2</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="3ec6f-113">Создает пространство имен концентраторов \` событий \` , MyNamespaceName в указанном географическом расположении \` MyLocation \` , в группе ресурсов \` MyResourceGroupName \` и AutoInflate включено с MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="3ec6f-114">Пример 3-Kafka Enabled Namespace</span><span class="sxs-lookup"><span data-stu-id="3ec6f-114">Example 3 - Kafka enabled namespace</span></span>
```
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 12
```

<span data-ttu-id="3ec6f-115">Создает пространство имен концентраторов \` событий \` , MyNamespaceName в указанном географическом расположении \` MyLocation \` , в группе ресурсов \` MyResourceGroupName \` с Kafka и AutoInflate.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="3ec6f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3ec6f-116">PARAMETERS</span></span>

### <span data-ttu-id="3ec6f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec6f-117">-DefaultProfile</span></span>
<span data-ttu-id="3ec6f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ec6f-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="3ec6f-119">-EnableAutoInflate</span></span>
<span data-ttu-id="3ec6f-120">Указывает, включена ли AutoInflate</span><span class="sxs-lookup"><span data-stu-id="3ec6f-120">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="3ec6f-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="3ec6f-121">-EnableKafka</span></span>
<span data-ttu-id="3ec6f-122">Включение и отключение Kafka для пространства имен</span><span class="sxs-lookup"><span data-stu-id="3ec6f-122">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="3ec6f-123">-Location</span><span class="sxs-lookup"><span data-stu-id="3ec6f-123">-Location</span></span>
<span data-ttu-id="3ec6f-124">Расположение пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-124">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="3ec6f-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="3ec6f-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="3ec6f-126">Верхний предел количества единиц пропускной способности при включенном AutoInflate значение должно находиться в диапазоне от 0 до 20 единиц пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="3ec6f-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3ec6f-127">-Name</span></span>
<span data-ttu-id="3ec6f-128">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="3ec6f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ec6f-129">-ResourceGroupName</span></span>
<span data-ttu-id="3ec6f-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3ec6f-130">Resource Group Name</span></span>

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

### <span data-ttu-id="3ec6f-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="3ec6f-131">-SkuCapacity</span></span>
<span data-ttu-id="3ec6f-132">Единицы пропускной способности eventhub.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-132">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="3ec6f-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3ec6f-133">-SkuName</span></span>
<span data-ttu-id="3ec6f-134">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-134">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="3ec6f-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="3ec6f-135">-Tag</span></span>
<span data-ttu-id="3ec6f-136">Хэш-таблицы, представляющие Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-136">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="3ec6f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ec6f-137">-Confirm</span></span>
<span data-ttu-id="3ec6f-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ec6f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ec6f-139">-WhatIf</span></span>
<span data-ttu-id="3ec6f-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ec6f-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ec6f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec6f-142">CommonParameters</span></span>
<span data-ttu-id="3ec6f-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3ec6f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec6f-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ec6f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec6f-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3ec6f-145">INPUTS</span></span>

### <span data-ttu-id="3ec6f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3ec6f-146">System.String</span></span>

### <span data-ttu-id="3ec6f-147">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3ec6f-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="3ec6f-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3ec6f-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3ec6f-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ec6f-149">OUTPUTS</span></span>

### <span data-ttu-id="3ec6f-150">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="3ec6f-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="3ec6f-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="3ec6f-151">NOTES</span></span>

## <span data-ttu-id="3ec6f-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ec6f-152">RELATED LINKS</span></span>
