---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: c75b456021368ea72a72bd0b0fea07a0f13d06dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730809"
---
# <span data-ttu-id="fd16f-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="fd16f-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="fd16f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd16f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd16f-103">Обновляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="fd16f-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="fd16f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd16f-104">SYNTAX</span></span>

### <span data-ttu-id="fd16f-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd16f-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd16f-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd16f-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd16f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd16f-107">DESCRIPTION</span></span>
<span data-ttu-id="fd16f-108">Командлет Set-AzEventHubNamespace обновляет свойства указанного пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="fd16f-108">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="fd16f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd16f-109">EXAMPLES</span></span>

### <span data-ttu-id="fd16f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fd16f-110">Example 1</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="fd16f-111">Обновляет состояние пространства имен \` MyNamespaceName \` для создания.</span><span class="sxs-lookup"><span data-stu-id="fd16f-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="fd16f-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fd16f-112">Example 2</span></span>
```
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="fd16f-113">Обновляет состояние пространства имен \` MyNamespaceName \` с AutoInflate = Enabled и MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="fd16f-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="fd16f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd16f-114">PARAMETERS</span></span>

### <span data-ttu-id="fd16f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd16f-115">-DefaultProfile</span></span>
<span data-ttu-id="fd16f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd16f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd16f-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="fd16f-117">-EnableAutoInflate</span></span>
<span data-ttu-id="fd16f-118">Указывает, включена ли AutoInflate</span><span class="sxs-lookup"><span data-stu-id="fd16f-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="fd16f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="fd16f-119">-Location</span></span>
<span data-ttu-id="fd16f-120">Расположение пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="fd16f-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="fd16f-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="fd16f-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="fd16f-122">Верхний предел количества единиц пропускной способности при включенном AutoInflate значение должно находиться в диапазоне от 0 до 20 единиц пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="fd16f-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="fd16f-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fd16f-123">-Name</span></span>
<span data-ttu-id="fd16f-124">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="fd16f-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="fd16f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd16f-125">-ResourceGroupName</span></span>
<span data-ttu-id="fd16f-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fd16f-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="fd16f-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fd16f-127">-SkuCapacity</span></span>
<span data-ttu-id="fd16f-128">Единицы пропускной способности eventhub.</span><span class="sxs-lookup"><span data-stu-id="fd16f-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="fd16f-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="fd16f-129">-SkuName</span></span>
<span data-ttu-id="fd16f-130">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="fd16f-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="fd16f-131">-State</span><span class="sxs-lookup"><span data-stu-id="fd16f-131">-State</span></span>
<span data-ttu-id="fd16f-132">Отключение и включение пространства имен.</span><span class="sxs-lookup"><span data-stu-id="fd16f-132">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="fd16f-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="fd16f-133">-Tag</span></span>
<span data-ttu-id="fd16f-134">Хэш-таблицы, представляющие тег ресурса.</span><span class="sxs-lookup"><span data-stu-id="fd16f-134">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="fd16f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd16f-135">-Confirm</span></span>
<span data-ttu-id="fd16f-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fd16f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd16f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd16f-137">-WhatIf</span></span>
<span data-ttu-id="fd16f-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd16f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd16f-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd16f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd16f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd16f-140">CommonParameters</span></span>
<span data-ttu-id="fd16f-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd16f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd16f-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd16f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd16f-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd16f-143">INPUTS</span></span>

### <span data-ttu-id="fd16f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fd16f-144">System.String</span></span>

### <span data-ttu-id="fd16f-145">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fd16f-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fd16f-146">System. Nullable "1 [[Microsoft. Azure. Commands. EventHub. NamespaceState., версия = 1.0.0.0, культура = нейтрально, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="fd16f-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="fd16f-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fd16f-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fd16f-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd16f-148">OUTPUTS</span></span>

### <span data-ttu-id="fd16f-149">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="fd16f-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="fd16f-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd16f-150">NOTES</span></span>

## <span data-ttu-id="fd16f-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd16f-151">RELATED LINKS</span></span>
