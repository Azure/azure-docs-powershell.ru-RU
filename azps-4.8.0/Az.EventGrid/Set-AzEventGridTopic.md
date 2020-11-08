---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244976"
---
# <span data-ttu-id="8c276-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="8c276-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="8c276-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c276-102">SYNOPSIS</span></span>
<span data-ttu-id="8c276-103">Задает свойства раздела сетки событий.</span><span class="sxs-lookup"><span data-stu-id="8c276-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="8c276-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c276-104">SYNTAX</span></span>

### <span data-ttu-id="8c276-105">TopicNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8c276-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c276-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c276-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8c276-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c276-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c276-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c276-108">DESCRIPTION</span></span>
<span data-ttu-id="8c276-109">Задает свойства раздела сетки событий.</span><span class="sxs-lookup"><span data-stu-id="8c276-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="8c276-110">Это можно использовать для замены тегов в разделе сетки событий.</span><span class="sxs-lookup"><span data-stu-id="8c276-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="8c276-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c276-111">EXAMPLES</span></span>

### <span data-ttu-id="8c276-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8c276-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="8c276-113">Задает свойства сетки событий \` в разделе элемент1 \` в группе ресурсов \` MyResourceGroupName \` , чтобы заменить Теги заданными тегами "Department" и "Environment".</span><span class="sxs-lookup"><span data-stu-id="8c276-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="8c276-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c276-114">PARAMETERS</span></span>

### <span data-ttu-id="8c276-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c276-115">-DefaultProfile</span></span>
<span data-ttu-id="8c276-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8c276-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c276-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="8c276-117">-InboundIpRule</span></span>
<span data-ttu-id="8c276-118">Хэш-таблица, представляющая список правил входящего трафика.</span><span class="sxs-lookup"><span data-stu-id="8c276-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="8c276-119">Каждое правило задает IP-адрес в нотации CIDR, например 10.0.0.0/8, и соответствующее действие, которое должно выполняться на основании совпадения или не совпадающей части IpMask.</span><span class="sxs-lookup"><span data-stu-id="8c276-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="8c276-120">Возможные значения действий: Allow only</span><span class="sxs-lookup"><span data-stu-id="8c276-120">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c276-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8c276-121">-InputObject</span></span>
<span data-ttu-id="8c276-122">Объект темы EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8c276-122">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c276-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8c276-123">-Name</span></span>
<span data-ttu-id="8c276-124">Название раздела EventGrid.</span><span class="sxs-lookup"><span data-stu-id="8c276-124">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c276-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="8c276-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="8c276-126">Этот тип определяет, разрешено ли трафик по общедоступной сети.</span><span class="sxs-lookup"><span data-stu-id="8c276-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="8c276-127">По умолчанию она включена.</span><span class="sxs-lookup"><span data-stu-id="8c276-127">By default it is enabled.</span></span> <span data-ttu-id="8c276-128">Вы можете дополнительно ограничиться определенными IP — настройкой параметров InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="8c276-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="8c276-129">Разрешенные значения отключены и включены.</span><span class="sxs-lookup"><span data-stu-id="8c276-129">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:
Accepted values: enabled, disabled

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:
Accepted values: enabled, disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c276-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c276-130">-ResourceGroupName</span></span>
<span data-ttu-id="8c276-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c276-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c276-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8c276-132">-ResourceId</span></span>
<span data-ttu-id="8c276-133">EventGrid темы (ResourceID).</span><span class="sxs-lookup"><span data-stu-id="8c276-133">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c276-134">-Тег</span><span class="sxs-lookup"><span data-stu-id="8c276-134">-Tag</span></span>
<span data-ttu-id="8c276-135">Хэш-таблицы, представляющие тег ресурса.</span><span class="sxs-lookup"><span data-stu-id="8c276-135">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c276-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c276-136">-Confirm</span></span>
<span data-ttu-id="8c276-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8c276-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c276-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c276-138">-WhatIf</span></span>
<span data-ttu-id="8c276-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8c276-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c276-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8c276-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c276-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c276-141">CommonParameters</span></span>
<span data-ttu-id="8c276-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c276-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c276-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c276-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c276-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c276-144">INPUTS</span></span>

### <span data-ttu-id="8c276-145">System. String</span><span class="sxs-lookup"><span data-stu-id="8c276-145">System.String</span></span>

### <span data-ttu-id="8c276-146">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="8c276-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="8c276-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8c276-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8c276-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c276-148">OUTPUTS</span></span>

### <span data-ttu-id="8c276-149">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="8c276-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="8c276-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c276-150">NOTES</span></span>

## <span data-ttu-id="8c276-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c276-151">RELATED LINKS</span></span>
