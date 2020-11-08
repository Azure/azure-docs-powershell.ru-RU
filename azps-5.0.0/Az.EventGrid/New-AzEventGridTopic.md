---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 402d781c32b98362d504dd5167024932d82e64fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248701"
---
# <span data-ttu-id="9d7ee-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="9d7ee-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="9d7ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7ee-103">Создание нового раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="9d7ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d7ee-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d7ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d7ee-105">DESCRIPTION</span></span>
<span data-ttu-id="9d7ee-106">Создание нового раздела сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="9d7ee-107">После создания темы приложение может публиковать события в конечной точке раздела.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="9d7ee-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d7ee-108">EXAMPLES</span></span>

### <span data-ttu-id="9d7ee-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9d7ee-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="9d7ee-110">Создание сетки событий в разделе \` элемент1 \` в указанном географическом расположении \` westus2 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="9d7ee-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="9d7ee-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9d7ee-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="9d7ee-112">Создает сетку событий \` в разделе элемент1 \` в указанном географическом расположении \` westus2 \` , в группе ресурсов \` MyResourceGroupName \` с заданными тегами "Отдел" и "среда".</span><span class="sxs-lookup"><span data-stu-id="9d7ee-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="9d7ee-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d7ee-113">PARAMETERS</span></span>

### <span data-ttu-id="9d7ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7ee-114">-DefaultProfile</span></span>
<span data-ttu-id="9d7ee-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9d7ee-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d7ee-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="9d7ee-116">-InboundIpRule</span></span>
<span data-ttu-id="9d7ee-117">Хэш-таблица, представляющая список правил входящего трафика.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="9d7ee-118">Каждое правило задает IP-адрес в нотации CIDR, например 10.0.0.0/8, и соответствующее действие, которое должно выполняться на основании совпадения или не совпадающей части IpMask.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="9d7ee-119">Возможные значения действий: Allow only</span><span class="sxs-lookup"><span data-stu-id="9d7ee-119">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ee-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="9d7ee-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="9d7ee-121">Хэш-таблица, представляющая поля сопоставления входных данных со значением по умолчанию в формате ключа = значения по разделителю.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="9d7ee-122">Разрешенные имена ключей: "Тема", "EventType" и "версия.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="9d7ee-123">Используется только в том случае, если InputSchemaHelp — customeventschema.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ee-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="9d7ee-124">-InputMappingField</span></span>
<span data-ttu-id="9d7ee-125">Хэш-таблица, представляющая поля сопоставления входных данных в формате ключа = значения с разделителем по местам.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="9d7ee-126">Разрешенные имена ключей: ID, тема, EventTime, тема, eventType и версия.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="9d7ee-127">Используется только в том случае, если InputSchemaHelp — customeventschema.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ee-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="9d7ee-128">-InputSchema</span></span>
<span data-ttu-id="9d7ee-129">Схема событий ввода для темы.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="9d7ee-130">Допустимые значения: eventgridschema, customeventschema или cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="9d7ee-131">Значение по умолчанию — eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-131">Default value is eventgridschema.</span></span> <span data-ttu-id="9d7ee-132">Обратите внимание, что если указан customeventschema, необходимо также указать InputMappingField или/и параметры InputMappingDefaultValue.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ee-133">-Location</span><span class="sxs-lookup"><span data-stu-id="9d7ee-133">-Location</span></span>
<span data-ttu-id="9d7ee-134">Расположение темы</span><span class="sxs-lookup"><span data-stu-id="9d7ee-134">The location of the topic</span></span>

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

### <span data-ttu-id="9d7ee-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9d7ee-135">-Name</span></span>
<span data-ttu-id="9d7ee-136">Название темы.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-136">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ee-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="9d7ee-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="9d7ee-138">Этот тип определяет, разрешено ли трафик по общедоступной сети.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="9d7ee-139">По умолчанию она включена.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-139">By default it is enabled.</span></span> <span data-ttu-id="9d7ee-140">Вы можете дополнительно ограничиться определенными IP — настройкой параметров InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="9d7ee-141">Разрешенные значения отключены и включены.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-141">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ee-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d7ee-142">-ResourceGroupName</span></span>
<span data-ttu-id="9d7ee-143">Группа ресурсов, в которой должен быть создан раздел.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-143">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ee-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="9d7ee-144">-Tag</span></span>
<span data-ttu-id="9d7ee-145">Хэш-таблицы, представляющие Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-145">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d7ee-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d7ee-146">-Confirm</span></span>
<span data-ttu-id="9d7ee-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d7ee-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d7ee-148">-WhatIf</span></span>
<span data-ttu-id="9d7ee-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d7ee-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d7ee-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7ee-151">CommonParameters</span></span>
<span data-ttu-id="9d7ee-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7ee-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d7ee-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7ee-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d7ee-154">INPUTS</span></span>

### <span data-ttu-id="9d7ee-155">System. String</span><span class="sxs-lookup"><span data-stu-id="9d7ee-155">System.String</span></span>

### <span data-ttu-id="9d7ee-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9d7ee-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9d7ee-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d7ee-157">OUTPUTS</span></span>

### <span data-ttu-id="9d7ee-158">Microsoft. Azure. Commands. EventGrid. Models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="9d7ee-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="9d7ee-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d7ee-159">NOTES</span></span>

## <span data-ttu-id="9d7ee-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d7ee-160">RELATED LINKS</span></span>
