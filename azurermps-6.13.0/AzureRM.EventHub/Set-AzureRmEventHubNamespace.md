---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespace.md
ms.openlocfilehash: 6fd3f000f7c91f0475cd18802dd6a9d096d35f5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566460"
---
# <span data-ttu-id="9f2c3-101">Set-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="9f2c3-101">Set-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="9f2c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="9f2c3-103">Обновляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-103">Updates the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f2c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f2c3-104">SYNTAX</span></span>

### <span data-ttu-id="9f2c3-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f2c3-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f2c3-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f2c3-106">AutoInflateParameterSet</span></span>
```
Set-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f2c3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f2c3-107">DESCRIPTION</span></span>
<span data-ttu-id="9f2c3-108">Командлет Set-AzureRmEventHubNamespace обновляет свойства указанного пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-108">The Set-AzureRmEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="9f2c3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f2c3-109">EXAMPLES</span></span>

### <span data-ttu-id="9f2c3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f2c3-110">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created
```

<span data-ttu-id="9f2c3-111">Обновляет состояние пространства имен \` MyNamespaceName \` для создания.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-111">Updates the state of namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="9f2c3-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9f2c3-112">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10
```

<span data-ttu-id="9f2c3-113">Обновляет состояние пространства имен \` MyNamespaceName \` с AutoInflate = Enabled и MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="9f2c3-113">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

## <span data-ttu-id="9f2c3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f2c3-114">PARAMETERS</span></span>

### <span data-ttu-id="9f2c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f2c3-115">-DefaultProfile</span></span>
<span data-ttu-id="9f2c3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f2c3-117">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="9f2c3-117">-EnableAutoInflate</span></span>
<span data-ttu-id="9f2c3-118">Указывает, включена ли AutoInflate</span><span class="sxs-lookup"><span data-stu-id="9f2c3-118">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="9f2c3-119">-Location</span><span class="sxs-lookup"><span data-stu-id="9f2c3-119">-Location</span></span>
<span data-ttu-id="9f2c3-120">Расположение пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-120">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="9f2c3-121">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="9f2c3-121">-MaximumThroughputUnits</span></span>
<span data-ttu-id="9f2c3-122">Верхний предел количества единиц пропускной способности при включенном AutoInflate значение должно находиться в диапазоне от 0 до 20 единиц пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-122">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="9f2c3-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9f2c3-123">-Name</span></span>
<span data-ttu-id="9f2c3-124">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-124">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="9f2c3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f2c3-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f2c3-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="9f2c3-127">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="9f2c3-127">-SkuCapacity</span></span>
<span data-ttu-id="9f2c3-128">Единицы пропускной способности eventhub.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-128">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="9f2c3-129">-SkuName</span><span class="sxs-lookup"><span data-stu-id="9f2c3-129">-SkuName</span></span>
<span data-ttu-id="9f2c3-130">Имя SKU пространства имен.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-130">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="9f2c3-131">-State</span><span class="sxs-lookup"><span data-stu-id="9f2c3-131">-State</span></span>
<span data-ttu-id="9f2c3-132">Отключение и включение пространства имен.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-132">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="9f2c3-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="9f2c3-133">-Tag</span></span>
<span data-ttu-id="9f2c3-134">Хэш-таблицы, представляющие тег ресурса.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-134">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="9f2c3-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f2c3-135">-Confirm</span></span>
<span data-ttu-id="9f2c3-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f2c3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f2c3-137">-WhatIf</span></span>
<span data-ttu-id="9f2c3-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f2c3-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f2c3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f2c3-140">CommonParameters</span></span>
<span data-ttu-id="9f2c3-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f2c3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f2c3-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f2c3-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f2c3-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f2c3-143">INPUTS</span></span>

### <span data-ttu-id="9f2c3-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9f2c3-144">System.String</span></span>

### <span data-ttu-id="9f2c3-145">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9f2c3-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9f2c3-146">System. Nullable "1 [[Microsoft. Azure. Commands. eventhub. System. NamespaceState, Microsoft. Azure. Commands. EventHub, Version = 0.6.7.0, культура = нейтрально, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="9f2c3-146">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.Commands.EventHub, Version=0.6.7.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9f2c3-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9f2c3-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9f2c3-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f2c3-148">OUTPUTS</span></span>

### <span data-ttu-id="9f2c3-149">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="9f2c3-149">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="9f2c3-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f2c3-150">NOTES</span></span>

## <span data-ttu-id="9f2c3-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f2c3-151">RELATED LINKS</span></span>
