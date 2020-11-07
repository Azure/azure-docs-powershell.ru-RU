---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: 99993a92179da1adaba068ae7bb525b5b2cca5df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720915"
---
# <span data-ttu-id="e7d82-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="e7d82-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="e7d82-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7d82-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d82-103">Обновляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="e7d82-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="e7d82-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7d82-104">SYNTAX</span></span>

### <span data-ttu-id="e7d82-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e7d82-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7d82-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7d82-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7d82-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7d82-107">DESCRIPTION</span></span>
<span data-ttu-id="e7d82-108">Командлет Set-AzEventHubNamespace обновляет свойства указанного пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="e7d82-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="e7d82-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7d82-109">EXAMPLES</span></span>

### <span data-ttu-id="e7d82-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7d82-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="e7d82-111">Обновляет Теги MyNamespaceName пространства имен \` \` для создания.</span><span class="sxs-lookup"><span data-stu-id="e7d82-111">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="e7d82-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e7d82-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
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
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="e7d82-113">Обновляет состояние пространства имен \` MyNamespaceName \` с AutoInflate = Enabled и MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="e7d82-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="e7d82-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7d82-114">PARAMETERS</span></span>

### <span data-ttu-id="e7d82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d82-115">-DefaultProfile</span></span>
<span data-ttu-id="e7d82-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7d82-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7d82-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="e7d82-117">-EnableAutoInflate</span></span>
<span data-ttu-id="e7d82-118">Указывает, включена ли AutoInflate</span><span class="sxs-lookup"><span data-stu-id="e7d82-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="e7d82-119">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="e7d82-119">-EnableKafka</span></span>
<span data-ttu-id="e7d82-120">Включение и отключение Kafka для пространства имен</span><span class="sxs-lookup"><span data-stu-id="e7d82-120">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="e7d82-121">-Location</span><span class="sxs-lookup"><span data-stu-id="e7d82-121">-Location</span></span>
<span data-ttu-id="e7d82-122">Расположение пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="e7d82-122">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="e7d82-123">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="e7d82-123">-MaximumThroughputUnits</span></span>
<span data-ttu-id="e7d82-124">Верхний предел количества единиц пропускной способности при включенном AutoInflate значение должно находиться в диапазоне от 0 до 20 единиц пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="e7d82-124">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d82-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e7d82-125">-Name</span></span>
<span data-ttu-id="e7d82-126">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="e7d82-126">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="e7d82-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7d82-127">-ResourceGroupName</span></span>
<span data-ttu-id="e7d82-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e7d82-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="e7d82-129">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e7d82-129">-SkuCapacity</span></span>
<span data-ttu-id="e7d82-130">Единицы пропускной способности eventhub.</span><span class="sxs-lookup"><span data-stu-id="e7d82-130">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="e7d82-131">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e7d82-131">-SkuName</span></span>
<span data-ttu-id="e7d82-132">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e7d82-132">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="e7d82-133">-State</span><span class="sxs-lookup"><span data-stu-id="e7d82-133">-State</span></span>
<span data-ttu-id="e7d82-134">Отключение и включение пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e7d82-134">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d82-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="e7d82-135">-Tag</span></span>
<span data-ttu-id="e7d82-136">Хэш-таблицы, представляющие тег ресурса.</span><span class="sxs-lookup"><span data-stu-id="e7d82-136">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7d82-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7d82-137">-Confirm</span></span>
<span data-ttu-id="e7d82-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e7d82-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7d82-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d82-139">-WhatIf</span></span>
<span data-ttu-id="e7d82-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e7d82-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7d82-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e7d82-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7d82-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d82-142">CommonParameters</span></span>
<span data-ttu-id="e7d82-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7d82-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d82-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7d82-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d82-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7d82-145">INPUTS</span></span>

### <span data-ttu-id="e7d82-146">System. String</span><span class="sxs-lookup"><span data-stu-id="e7d82-146">System.String</span></span>

### <span data-ttu-id="e7d82-147">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e7d82-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e7d82-148">System. Nullable "1 [[Microsoft. Azure. Commands. EventHub. NamespaceState., версия = 1.3.0.0, культура = нейтрально, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="e7d82-148">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e7d82-149">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e7d82-149">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e7d82-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7d82-150">OUTPUTS</span></span>

### <span data-ttu-id="e7d82-151">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e7d82-151">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="e7d82-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7d82-152">NOTES</span></span>

## <span data-ttu-id="e7d82-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7d82-153">RELATED LINKS</span></span>
