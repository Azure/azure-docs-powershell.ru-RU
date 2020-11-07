---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: bbe0f406232086fc0441281ae150f95e2c8eb0a4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912036"
---
# <span data-ttu-id="f4633-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="f4633-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="f4633-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4633-102">SYNOPSIS</span></span>
<span data-ttu-id="f4633-103">Создает пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="f4633-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="f4633-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4633-104">SYNTAX</span></span>

### <span data-ttu-id="f4633-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4633-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4633-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4633-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4633-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4633-107">DESCRIPTION</span></span>
<span data-ttu-id="f4633-108">Командлет New-AzEventHubNamespace создает новое пространство имен концентраторов событий типа.</span><span class="sxs-lookup"><span data-stu-id="f4633-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="f4633-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4633-109">EXAMPLES</span></span>

### <span data-ttu-id="f4633-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f4633-110">Example 1</span></span>                                           
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

<span data-ttu-id="f4633-111">Создает пространство имен MyNamespaceNameных концентраторов событий \` \` в указанном географическом расположении \` MyLocation \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="f4633-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f4633-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f4633-112">Example 2</span></span>
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

<span data-ttu-id="f4633-113">Создает пространство имен концентраторов \` событий \` , MyNamespaceName в указанном географическом расположении \` MyLocation \` , в группе ресурсов \` MyResourceGroupName \` и AutoInflate включено с MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="f4633-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="f4633-114">Пример 3-Kafka Enabled Namespace</span><span class="sxs-lookup"><span data-stu-id="f4633-114">Example 3 - Kafka enabled namespace</span></span>
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

<span data-ttu-id="f4633-115">Создает пространство имен концентраторов \` событий \` , MyNamespaceName в указанном географическом расположении \` MyLocation \` , в группе ресурсов \` MyResourceGroupName \` с Kafka и AutoInflate.</span><span class="sxs-lookup"><span data-stu-id="f4633-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

## <span data-ttu-id="f4633-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4633-116">PARAMETERS</span></span>

### <span data-ttu-id="f4633-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4633-117">-DefaultProfile</span></span>
<span data-ttu-id="f4633-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4633-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4633-119">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="f4633-119">-EnableAutoInflate</span></span>
<span data-ttu-id="f4633-120">Указывает, включена ли AutoInflate</span><span class="sxs-lookup"><span data-stu-id="f4633-120">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="f4633-121">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="f4633-121">-EnableKafka</span></span>
<span data-ttu-id="f4633-122">Включение и отключение Kafka для пространства имен</span><span class="sxs-lookup"><span data-stu-id="f4633-122">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="f4633-123">-Location</span><span class="sxs-lookup"><span data-stu-id="f4633-123">-Location</span></span>
<span data-ttu-id="f4633-124">Расположение пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="f4633-124">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="f4633-125">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="f4633-125">-MaximumThroughputUnits</span></span>
<span data-ttu-id="f4633-126">Верхний предел количества единиц пропускной способности при включенном AutoInflate значение должно находиться в диапазоне от 0 до 20 единиц пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="f4633-126">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="f4633-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4633-127">-Name</span></span>
<span data-ttu-id="f4633-128">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="f4633-128">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="f4633-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4633-129">-ResourceGroupName</span></span>
<span data-ttu-id="f4633-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f4633-130">Resource Group Name</span></span>

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

### <span data-ttu-id="f4633-131">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="f4633-131">-SkuCapacity</span></span>
<span data-ttu-id="f4633-132">Единицы пропускной способности eventhub.</span><span class="sxs-lookup"><span data-stu-id="f4633-132">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="f4633-133">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f4633-133">-SkuName</span></span>
<span data-ttu-id="f4633-134">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="f4633-134">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="f4633-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="f4633-135">-Tag</span></span>
<span data-ttu-id="f4633-136">Хэш-таблицы, представляющие Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4633-136">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="f4633-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4633-137">-Confirm</span></span>
<span data-ttu-id="f4633-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4633-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4633-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4633-139">-WhatIf</span></span>
<span data-ttu-id="f4633-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4633-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4633-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4633-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4633-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4633-142">CommonParameters</span></span>
<span data-ttu-id="f4633-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4633-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4633-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4633-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4633-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4633-145">INPUTS</span></span>

### <span data-ttu-id="f4633-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f4633-146">System.String</span></span>

### <span data-ttu-id="f4633-147">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f4633-147">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f4633-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f4633-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f4633-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4633-149">OUTPUTS</span></span>

### <span data-ttu-id="f4633-150">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="f4633-150">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="f4633-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4633-151">NOTES</span></span>

## <span data-ttu-id="f4633-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4633-152">RELATED LINKS</span></span>
