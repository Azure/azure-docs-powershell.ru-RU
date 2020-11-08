---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 6340db7446671660df08449529b6678cf79a2af9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243592"
---
# <span data-ttu-id="a6c4b-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="a6c4b-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="a6c4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a6c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c4b-103">Создает новый домен сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="a6c4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a6c4b-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6c4b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6c4b-105">DESCRIPTION</span></span>
<span data-ttu-id="a6c4b-106">Создает новый домен сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="a6c4b-107">После создания домена приложение может публиковать события в конечной точке раздела.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="a6c4b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a6c4b-108">EXAMPLES</span></span>

### <span data-ttu-id="a6c4b-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6c4b-109">Example 1</span></span>

<span data-ttu-id="a6c4b-110">Создание Domain1 домена событий \` \` в указанном географическом расположении \` westus2 \` в группе ресурсов \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="a6c4b-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="a6c4b-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a6c4b-111">Example 2</span></span>

<span data-ttu-id="a6c4b-112">Создание Domain1 домена событий \` \` в указанном географическом расположении \` westus2 в \` группе ресурсов \` MyResourceGroupName \` с заданными тегами "Отдел" и "среда".</span><span class="sxs-lookup"><span data-stu-id="a6c4b-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="a6c4b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a6c4b-113">PARAMETERS</span></span>

### <span data-ttu-id="a6c4b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c4b-114">-DefaultProfile</span></span>
<span data-ttu-id="a6c4b-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6c4b-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="a6c4b-116">-InboundIpRule</span></span>
<span data-ttu-id="a6c4b-117">Хэш-таблица, представляющая список правил входящего трафика.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="a6c4b-118">Каждое правило задает IP-адрес в нотации CIDR, например 10.0.0.0/8, и соответствующее действие, которое должно выполняться на основании совпадения или не совпадающей части IpMask.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="a6c4b-119">Возможные значения действий: Allow only</span><span class="sxs-lookup"><span data-stu-id="a6c4b-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="a6c4b-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="a6c4b-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="a6c4b-121">Хэш-таблица, представляющая поля сопоставления входных данных со значением по умолчанию в формате ключа = значения по разделителю.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="a6c4b-122">Разрешенные имена ключей: "Тема", "EventType" и "версия.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="a6c4b-123">Используется только в том случае, если InputSchemaHelp — customeventschema.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="a6c4b-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="a6c4b-124">-InputMappingField</span></span>
<span data-ttu-id="a6c4b-125">Хэш-таблица, представляющая поля сопоставления входных данных в формате ключа = значения с разделителем по местам.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="a6c4b-126">Разрешенные имена ключей: ID, тема, EventTime, тема, eventType и версия.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="a6c4b-127">Используется только в том случае, если InputSchemaHelp — customeventschema.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="a6c4b-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="a6c4b-128">-InputSchema</span></span>
<span data-ttu-id="a6c4b-129">Схема событий ввода для темы.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="a6c4b-130">Допустимые значения: eventgridschema, customeventschema или cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="a6c4b-131">Значение по умолчанию — eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-131">Default value is eventgridschema.</span></span> <span data-ttu-id="a6c4b-132">Обратите внимание, что если указан customeventschema, необходимо также указать InputMappingField или/и параметры InputMappingDefaultValue.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="a6c4b-133">-Location</span><span class="sxs-lookup"><span data-stu-id="a6c4b-133">-Location</span></span>
<span data-ttu-id="a6c4b-134">Расположение домена.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-134">The location of the domain.</span></span>

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

### <span data-ttu-id="a6c4b-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a6c4b-135">-Name</span></span>
<span data-ttu-id="a6c4b-136">EventGrid Domain Name (доменное имя).</span><span class="sxs-lookup"><span data-stu-id="a6c4b-136">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6c4b-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="a6c4b-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="a6c4b-138">Этот тип определяет, разрешено ли трафик по общедоступной сети.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="a6c4b-139">По умолчанию она включена.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-139">By default it is enabled.</span></span> <span data-ttu-id="a6c4b-140">Вы можете дополнительно ограничиться определенными IP — настройкой параметров InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="a6c4b-141">Разрешенные значения отключены и включены.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="a6c4b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6c4b-142">-ResourceGroupName</span></span>
<span data-ttu-id="a6c4b-143">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="a6c4b-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="a6c4b-144">-Tag</span></span>
<span data-ttu-id="a6c4b-145">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-145">Hashtable which represents resource Tags.</span></span>

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

### <span data-ttu-id="a6c4b-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6c4b-146">-Confirm</span></span>
<span data-ttu-id="a6c4b-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6c4b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6c4b-148">-WhatIf</span></span>
<span data-ttu-id="a6c4b-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6c4b-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6c4b-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c4b-151">CommonParameters</span></span>
<span data-ttu-id="a6c4b-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a6c4b-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c4b-153">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6c4b-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c4b-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a6c4b-154">INPUTS</span></span>

### <span data-ttu-id="a6c4b-155">System. String</span><span class="sxs-lookup"><span data-stu-id="a6c4b-155">System.String</span></span>

### <span data-ttu-id="a6c4b-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a6c4b-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a6c4b-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6c4b-157">OUTPUTS</span></span>

### <span data-ttu-id="a6c4b-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="a6c4b-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="a6c4b-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="a6c4b-159">NOTES</span></span>

## <span data-ttu-id="a6c4b-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6c4b-160">RELATED LINKS</span></span>
